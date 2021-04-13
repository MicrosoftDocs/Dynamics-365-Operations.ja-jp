---
title: RunBase クラスの拡張
description: このトピックには、RunBase クラスを拡張できる方法を示した例が徹底的に含まれています。
author: MichaelFruergaardPontoppidan
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: 8DA4DA85-0C2D-4CAF-B350-DAC9C1BE4DF9
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 8e1803d9f7113dd5085c704db44c3f0ceaf47815
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749648"
---
# <a name="extend-the-runbase-class"></a>RunBase クラスの拡張

[!include [banner](../includes/banner.md)]

アプリケーション スイートの機能を拡張するとき、**RunBase** クラスを拡張するクラスに遭遇します。 このトピックでは、**RunBase** クラスをエンド・ツー・エンドで拡張する方法を示します。

たとえば、SysUserLogCleanup クラスを拡張します。 すぐに使えるこのクラスは、SysUserLog テーブルからレコードを削除できます。 ただし、削除する前に、これらのレコードを別のテーブルにアーカイブします。

SysUserLogCleanup クラスは、**RunBase** クラスです。 **RunBase** クラスには、クラスを実行する前にユーザーにパラメーターを求めるダイアログ ボックスがあります。 この例では、ダイアログ ボックスに切り替えボタン コントロールを追加し、コントロールの値を取得して実行メソッドの値を処理し、さらに値が pack および unpack メソッドを介してシリアル化されるどうかを確認します。 シリアル化により、ダイアログ ボックスを再び開いた場合にユーザーの最後の選択が再表示されることが保証されます。 また、クラスがバックグラウンドで実行される場合に、設定が適用されていることを保証することもできます。

他の最終的な拡張機能との衝突を避けるために、次のベストプラクティスに従っています。

- **接頭語メンバーおよびメソッド**。 例では、接頭語「my」が使用されます。 このプラクティスは、他の拡張機能と拡張されたクラスの将来のバージョンとの名前の衝突を防ぐために重要です。

- **RunBase.packExtension() および RunBase.unpackExtension() の使用**。 これらのメソッドは、非直列的な方法でシリアル化を提供します。 それらは同じクラスの複数の拡張のシリアル化を可能にします。 これらのメソッドは、プラットフォーム Update 5 以降で使用できます。

次の例は、このシナリオを実装する方法を示しています。

```xpp
[ExtensionOf(classStr(SysUserLogCleanup))]
final class MySysUserLogCleanup_Extension
{
    // static members
    static private SysUserLogCleanup myRunningInstance;

    // Extending class state...
    private boolean myArchive;
    private DialogField myDialogArchive;
    #define.CurrentVersion(1)
    #localmacro.CurrentList
        myArchive
    #endmacro

    public Object dialog()
    {
        Dialog dialog = next dialog();

        myDialogArchive = dialog.addField(extendedtypestr(NoYesId), "Archive");
        myDialogArchive.value(myArchive);

        return dialog;
    }

    public boolean getFromDialog()
    {
        boolean result = next getFromDialog();
        myArchive = myDialogArchive.value();
        return result;
    }
    
    public void initParmDefault()
    {
        next initParmDefault();
        myArchive = true;
    }    

    public void run()
    {
        try
        {
            myRunningInstance = this;
            next run();
        }
        finally
        {
            myRunningInstance = null;
        }
    }

    public container pack()
    {
        container packedClass = next pack();
        return SysPackExtensions::appendExtension(packedClass, classStr(MySysUserLogCleanup_Extension), this.myPack());
    }

    private boolean myUnpack(container packedClass)
    {
        Integer version = RunBase::getVersion(packedClass);
        switch (version)
        {
            case #CurrentVersion:
                [version, #currentList] = packedClass;
                break;
            default:
                return false;
        }
        return true;
    }

    private container myPack()
    {
        return [#CurrentVersion, #CurrentList];
    }

    public boolean unpack(container _packedClass)
    {
        boolean result = next unpack(_packedClass);

        if (result)
        {
            container myState = SysPackExtensions::findExtension(_packedClass, classStr(MySysUserLogCleanup_Extension));
            //Also unpack the extension
            if (!this.myUnpack(myState))
            {
                result = false;
            }
        }

        return result;
    }
    
    private void myArchiveUserLog(SysUserLog _userLog)
    {
        if (myArchive)
        {
            //...
        }
    }

    // Wire up event handler for deletion of the record
    [DataEventHandler(tableStr(SysUserLog), DataEventType::Deleting)]
    static public void SysUserLog_onDeleting(Common _sender, DataEventArgs _e)
    {
        if (myRunningInstance)
        {
            myRunningInstance.myArchiveUserLog(_sender as SysUserLog);
        }
    }
}
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]