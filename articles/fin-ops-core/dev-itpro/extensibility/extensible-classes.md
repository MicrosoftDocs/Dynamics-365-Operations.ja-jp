---
title: 拡張可能クラスの書き込み
description: このトピックでは、拡張可能クラスを書き込む方法について説明します。
author: smithanataraj
manager: AnnBe
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: Smitha Nataraj, Lars-Bo
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: fcb57b6164546d154b1496d0d42f2d2af4e94bef
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191637"
---
# <a name="write-extensible-classes"></a><span data-ttu-id="ed26f-103">拡張可能クラスの書き込み</span><span class="sxs-lookup"><span data-stu-id="ed26f-103">Write extensible classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed26f-104">クラスとそのメソッドには、単一の責任が必要です。</span><span class="sxs-lookup"><span data-stu-id="ed26f-104">A class and its methods should have a single responsibility.</span></span> <span data-ttu-id="ed26f-105">長期的な変更に耐えるクラスをデザインするために以下の点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="ed26f-105">Keep the following in mind in order to design classes that are resilient to changes in the long run.</span></span> <span data-ttu-id="ed26f-106">クラスに必要なもの:</span><span class="sxs-lookup"><span data-stu-id="ed26f-106">Class should have:</span></span>

+ <span data-ttu-id="ed26f-107">明確な目的</span><span class="sxs-lookup"><span data-stu-id="ed26f-107">A clear purpose</span></span>
+ <span data-ttu-id="ed26f-108">適切な名前 (クラス名およびメソッド名)</span><span class="sxs-lookup"><span data-stu-id="ed26f-108">Good names (class name and method names)</span></span>
+ <span data-ttu-id="ed26f-109">拡張する必要があるメソッドのみ拡張性のために公開されます。つまり、主要なルールは、できる限り拡張を最小限にすることです。</span><span class="sxs-lookup"><span data-stu-id="ed26f-109">Only methods that should be extended are exposed for extensibility, i.e. the key rule is allow extending as little as necessary.</span></span>
    - <span data-ttu-id="ed26f-110">すべてのパブリックおよび保護メソッドが X++ における拡張性ポイントとなります。</span><span class="sxs-lookup"><span data-stu-id="ed26f-110">Every public and protected method is an extensibility point in X++.</span></span> <span data-ttu-id="ed26f-111">新しいメソッドを導入するたびに、ダウンストリーム ユーザーはメソッドに追加のロジックを挿入する新しい方法を取得します。</span><span class="sxs-lookup"><span data-stu-id="ed26f-111">Every time that a new method is introduced, downstream consumers get a new way to inject additional logic into the method.</span></span>

### <a name="example"></a><span data-ttu-id="ed26f-112">例</span><span class="sxs-lookup"><span data-stu-id="ed26f-112">Example</span></span>

<span data-ttu-id="ed26f-113">**拡張不可コード**</span><span class="sxs-lookup"><span data-stu-id="ed26f-113">**Non-extensible code**</span></span>

```
    void calculatePrice(SalesLine _saleLine, AmountMST _amount)
    {
        // cannot add extra condition if needed
        if(_saleLine.QtyOrdered > 0 && _saleLine.SalesType == SalesType::Sales)
        {
            ttsbegin;
            // calculation of SalesPrice is locked and cannot be extended
            _saleLine.SalesPrice = _saleLine.QtyOrdered * _amount;
            _saleLine.update();
            ttscommit;
        }
    }
```

<span data-ttu-id="ed26f-114">**拡張可能コード**</span><span class="sxs-lookup"><span data-stu-id="ed26f-114">**Extensible code**</span></span>

```
 protected boolean canUpdateSalesPrice(SalesLine _saleLine)
    {
        return (_saleLine.QtyOrdered > 0 &&
    _saleLine.SalesType == SalesType::Sales);
    }
 
    protected SalesPrice calculateSalesPrice(
    SalesLine _saleLine, AmountMST _amount)
    {
        return _saleLine.QtyOrdered * _amount;
    }
 
    public void updateSalesPrice(SalesLine _saleLine, AmountMST _amount)
    {
        // extra condition can be added in CoC on the method
        if(this.canUpdateSalesPrice(_saleLine))
        {
            ttsbegin;
            // extra calculation/value can be added in CoC on the method
            _saleLine.SalesPrice = this.calculateSalesPrice(_saleLine, _amount);
            _saleLine.update();
            ttscommit;
        }
    }
```

## <a name="class-hierarchies"></a><span data-ttu-id="ed26f-115">クラス階層</span><span class="sxs-lookup"><span data-stu-id="ed26f-115">Class hierarchies</span></span>
<span data-ttu-id="ed26f-116">出荷時のパターンを使用できる新規または既存のクラス階層の場合、SysExtension フレームワークにより簡単に拡張可能になります。</span><span class="sxs-lookup"><span data-stu-id="ed26f-116">For new or existing class hierarchies where a factory pattern can be used, the SysExtension framework enables easy extensions.</span></span> <span data-ttu-id="ed26f-117">これらの拡張は完全に切り離されるため、基本クラスに変更を加えなくても新しいサブクラスを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ed26f-117">Because these extensions are truly decoupled, new subclasses can be added without requiring any changes to the base class.</span></span> <span data-ttu-id="ed26f-118">したがってより少ないコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="ed26f-118">Therefore, less code is required.</span></span> <span data-ttu-id="ed26f-119">さらに、コストラクトのコントラクトが変わらないので、パブリック アプリケーション プログラミング インターフェイス (API) への変更はありません。</span><span class="sxs-lookup"><span data-stu-id="ed26f-119">Additionally, because the contract of the construct remains the same, there is no change to the public application programming interface (API).</span></span> <span data-ttu-id="ed26f-120">したがって、リファクタリングは低リスクです。</span><span class="sxs-lookup"><span data-stu-id="ed26f-120">Therefore, refactoring involves low risk.</span></span>
    
<span data-ttu-id="ed26f-121">いくつかの既存のファクトリ メソッドは、インスタンス コンストラクターを使用してサブクラスをインスタンス化しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ed26f-121">Some existing factory methods might not instantiate subclasses by using the instance constructor.</span></span> <span data-ttu-id="ed26f-122">代わりに、**コンストラクト**などの静的コンストラクターを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="ed26f-122">Instead, they might call a static constructor, such as **construct**.</span></span> <span data-ttu-id="ed26f-123">これらのファクトリ メソッドに SysExtension フレームワークが使用される場合、重大な変更が発生します。サブクラスの静的コンストラクターが呼び出されなくなるためです。</span><span class="sxs-lookup"><span data-stu-id="ed26f-123">If the SysExtension framework is used for these factory methods, a breaking change occurs, because the static constructors on the subclasses are no longer invoked.</span></span> <span data-ttu-id="ed26f-124">このような場合は、既定のケースにのみ SysExtension フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="ed26f-124">In these situations, use the SysExtension framework only for the default case.</span></span>
    
<span data-ttu-id="ed26f-125">クラス階層構造の詳細については、次のブログ記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed26f-125">For more information about class hierarchies, see the following blog posts:</span></span>

+ [<span data-ttu-id="ed26f-126">SysExtension フレームワーク – 問題発生時</span><span class="sxs-lookup"><span data-stu-id="ed26f-126">SysExtension Framework – to the rescue</span></span>](https://blogs.msdn.microsoft.com/mfp/2013/06/12/sysextension-framework-to-the-rescue/)
+ [<span data-ttu-id="ed26f-127">Dynamics 365 for Finance and Operations への拡張機能のご要望の採用 #2 - SysExtension フレームワーク</span><span class="sxs-lookup"><span data-stu-id="ed26f-127">Embrace the extensions mindset with Dynamics 365 for Finance and Operations #2 – SysExtension framework</span></span>](https://blogs.msdn.microsoft.com/axinthefield/embrace-the-extensions-mindset-with-dynamics-365-for-finance-and-operations-2-sysextension-framework/)

## <a name="deprecation"></a><span data-ttu-id="ed26f-128">廃止</span><span class="sxs-lookup"><span data-stu-id="ed26f-128">Deprecation</span></span>
<span data-ttu-id="ed26f-129">クラスまたはパブリックまたは保護メソッドが不要になった場合、必ずまず警告を使用し、メソッドが廃止されたことをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="ed26f-129">If a class or a public or protected method is no longer required, always use a warning first to notify consumers that the method is obsolete.</span></span> <span data-ttu-id="ed26f-130">次に、すべてのユーザーは、変更または新しい API を取り込むことができ、メソッドを廃止できます。</span><span class="sxs-lookup"><span data-stu-id="ed26f-130">Then, when all consumers have had the chance to uptake the changes or the new API, the method can be deprecated.</span></span> <span data-ttu-id="ed26f-131">クラスおよびメソッドの廃止 (または、それ以外の場合はクラス メンバーの削除) は、大きな変更点です。</span><span class="sxs-lookup"><span data-stu-id="ed26f-131">Deprecation of classes and methods (or removal of class members in other cases) is a breaking change.</span></span> <span data-ttu-id="ed26f-132">詳細については、[重大な変更](breaking-changes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed26f-132">For more information, see [Breaking changes](breaking-changes.md).</span></span>