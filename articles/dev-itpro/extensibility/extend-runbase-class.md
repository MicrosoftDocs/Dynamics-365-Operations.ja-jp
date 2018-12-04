---
title: "RunBase クラスの拡張"
description: "このトピックには、RunBase クラスを拡張できる方法を示した例が徹底的に含まれています。"
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 8DA4DA85-0C2D-4CAF-B350-DAC9C1BE4DF9
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 2a8850211e35950dfad38ff4de8565c811f5ee08
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

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

```
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

    // Adding new instance methods
    private void myDialog(Dialog _dialog)
    {
        myDialogArchive = _dialog.addField(extendedtypestr(NoYesId), "Archive");
        myDialogArchive.value(myArchive);
    }
    private void myGetFromDialog()
    {
        myArchive = myDialogArchive.value();
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
    private void myInitParmDefault()
    {
        myArchive = true;
    }
    private void myArchiveUserLog(SysUserLog _userLog)
    {
        if (myArchive)
        {
            //...
        }
    }

    // Wiring up event handlers...
    [PostHandlerFor(classStr(SysUserLogCleanup), methodStr(SysUserLogCleanup, dialog))]
    public static void SysUserLogCleanup_Post_Dialog(XppPrePostArgs _args)
    {
        Dialog dialog = _args.getReturnValue();
        SysUserLogCleanup instance = _args.getThis() as SysUserLogCleanup;
        instance.myDialog(dialog);
    }
    [PostHandlerFor(classStr(SysUserLogCleanup), methodStr(SysUserLogCleanup, getFromDialog))]
    public static void SysUserLogCleanup_Post_GetFromDialog(XppPrePostArgs _args)
    {
        SysUserLogCleanup instance = _args.getThis() as SysUserLogCleanup;
        instance.myGetFromDialog();
    }
    [PostHandlerFor(classStr(SysUserLogCleanup), methodStr(SysUserLogCleanup, pack))]
    public static void SysUserLogCleanup_Post_pack(XppPrePostArgs _args)
    {
        SysUserLogCleanup instance = _args.getThis() as SysUserLogCleanup;
        //Also pack the extension
        instance.packExtension(_args, classStr(MySysUserLogCleanup_Extension), instance.myPack());
    }
    [PostHandlerFor(classStr(SysUserLogCleanup), methodStr(SysUserLogCleanup, unpack))]
    public static void SysUserLogCleanup_Post_unpack(XppPrePostArgs _args)
    {
        SysUserLogCleanup instance = _args.getThis() as SysUserLogCleanup;
        container myState = instance.unpackExtension(_args, classStr(MySysUserLogCleanup_Extension));
        //Also unpack the extension
        if (!instance.myUnpack(myState))
        {
            //Extension couldn't be unpacked - return false to trigger initParmDefault() gets called
            _args.setReturnValue(false);
        }
    }
    [PostHandlerFor(classStr(SysUserLogCleanup), methodStr(SysUserLogCleanup, initParmDefault))]
    public static void SysUserLogCleanup_Post_initParmDefault(XppPrePostArgs _args)
    {
        SysUserLogCleanup instance = _args.getThis() as SysUserLogCleanup;
        instance.myInitParmDefault();
    }
    [PreHandlerFor(classStr(SysUserLogCleanup), methodStr(SysUserLogCleanup, run))]
    public static void SysUserLogCleanup_Pre_run(XppPrePostArgs _args)
    {
        //Store a static reference, so we can call it from SysUserLog_onDeleting.
        myRunningInstance = _args.getThis() as SysUserLogCleanup;
    }
    [PostHandlerFor(classStr(SysUserLogCleanup), methodStr(SysUserLogCleanup, run))]
    public static void SysUserLogCleanup_Post_run(XppPrePostArgs _args)
    {
        //Running complete 
        myRunningInstance = null;
    }

    // Wiring up event handler for deletion of the record
    [DataEventHandler(tableStr(SysUserLog), DataEventType::Deleting)]
    static public void SysUserLog_onDeleting(Common _sender, DataEventArgs _e)
    {
        if (runningInstance)
        {
            myRunningInstance.myArchiveUserLog(_sender as SysUserLog);
        }
    }
}
```



