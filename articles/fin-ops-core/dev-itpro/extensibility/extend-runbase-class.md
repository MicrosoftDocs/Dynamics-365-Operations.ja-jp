---
title: RunBase クラスの拡張
description: このトピックには、RunBase クラスを拡張できる方法を示した例が徹底的に含まれています。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 8DA4DA85-0C2D-4CAF-B350-DAC9C1BE4DF9
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 0c5d218053647ac230d92e4e28a280ade2d554a3
ms.sourcegitcommit: 9f90b194c0fc751d866d3d24d57ecf1b3c5053a1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3033020"
---
# <a name="extend-the-runbase-class"></a><span data-ttu-id="fd86e-103">RunBase クラスの拡張</span><span class="sxs-lookup"><span data-stu-id="fd86e-103">Extend the RunBase class</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd86e-104">アプリケーション スイートの機能を拡張するとき、**RunBase** クラスを拡張するクラスに遭遇します。</span><span class="sxs-lookup"><span data-stu-id="fd86e-104">When you extend functionality of the application suite, you will encounter classes that extend the **RunBase** class.</span></span> <span data-ttu-id="fd86e-105">このトピックでは、**RunBase** クラスをエンド・ツー・エンドで拡張する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="fd86e-105">This topic shows how a **RunBase** class can be augmented end to end.</span></span>

<span data-ttu-id="fd86e-106">たとえば、SysUserLogCleanup クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="fd86e-106">For example, you want to extend the SysUserLogCleanup class.</span></span> <span data-ttu-id="fd86e-107">すぐに使えるこのクラスは、SysUserLog テーブルからレコードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="fd86e-107">Out of the box, this class can delete records from the SysUserLog table.</span></span> <span data-ttu-id="fd86e-108">ただし、削除する前に、これらのレコードを別のテーブルにアーカイブします。</span><span class="sxs-lookup"><span data-stu-id="fd86e-108">However, you want to archive these records to a different table before they are deleted.</span></span>

<span data-ttu-id="fd86e-109">SysUserLogCleanup クラスは、**RunBase** クラスです。</span><span class="sxs-lookup"><span data-stu-id="fd86e-109">The SysUserLogCleanup class is a **RunBase** class.</span></span> <span data-ttu-id="fd86e-110">**RunBase** クラスには、クラスを実行する前にユーザーにパラメーターを求めるダイアログ ボックスがあります。</span><span class="sxs-lookup"><span data-stu-id="fd86e-110">The **RunBase** class has a dialog box, where the user is prompted for parameters before the class is run.</span></span> <span data-ttu-id="fd86e-111">この例では、ダイアログ ボックスに切り替えボタン コントロールを追加し、コントロールの値を取得して実行メソッドの値を処理し、さらに値が pack および unpack メソッドを介してシリアル化されるどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="fd86e-111">For this example, we will add a toggle button control to the dialog box, get the value of the control, act on the value in the run method, and make sure that the value is serialized via the pack and unpack methods.</span></span> <span data-ttu-id="fd86e-112">シリアル化により、ダイアログ ボックスを再び開いた場合にユーザーの最後の選択が再表示されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="fd86e-112">Serialization helps guarantee that the user’s last selection is presented again if the dialog box is reopened.</span></span> <span data-ttu-id="fd86e-113">また、クラスがバックグラウンドで実行される場合に、設定が適用されていることを保証することもできます。</span><span class="sxs-lookup"><span data-stu-id="fd86e-113">It also helps guarantee that the settings are applied if the class is run in the background.</span></span>

<span data-ttu-id="fd86e-114">他の最終的な拡張機能との衝突を避けるために、次のベストプラクティスに従っています。</span><span class="sxs-lookup"><span data-stu-id="fd86e-114">To avoid collisions with other eventual extensions, we followed these best practices:</span></span>

- <span data-ttu-id="fd86e-115">**接頭語メンバーおよびメソッド**。</span><span class="sxs-lookup"><span data-stu-id="fd86e-115">**Prefix members and methods**.</span></span> <span data-ttu-id="fd86e-116">例では、接頭語「my」が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd86e-116">In the example, the prefix “my” is used.</span></span> <span data-ttu-id="fd86e-117">このプラクティスは、他の拡張機能と拡張されたクラスの将来のバージョンとの名前の衝突を防ぐために重要です。</span><span class="sxs-lookup"><span data-stu-id="fd86e-117">This practice is important, because it helps prevent name clashes with other extensions and future versions of the augmented class.</span></span>

- <span data-ttu-id="fd86e-118">**RunBase.packExtension() および RunBase.unpackExtension() の使用**。</span><span class="sxs-lookup"><span data-stu-id="fd86e-118">**Use RunBase.packExtension() and RunBase.unpackExtension()**.</span></span> <span data-ttu-id="fd86e-119">これらのメソッドは、非直列的な方法でシリアル化を提供します。</span><span class="sxs-lookup"><span data-stu-id="fd86e-119">These methods provide serialization in a nonintrusive manner.</span></span> <span data-ttu-id="fd86e-120">それらは同じクラスの複数の拡張のシリアル化を可能にします。</span><span class="sxs-lookup"><span data-stu-id="fd86e-120">They enable serialization of multiple extensions of the same class.</span></span> <span data-ttu-id="fd86e-121">これらのメソッドは、プラットフォーム Update 5 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="fd86e-121">The methods are available starting in Platform Update 5.</span></span>

<span data-ttu-id="fd86e-122">次の例は、このシナリオを実装する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fd86e-122">The following example shows how to implement this scenario.</span></span>

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


