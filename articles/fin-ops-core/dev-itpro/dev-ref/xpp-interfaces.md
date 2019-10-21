---
title: X++ インターフェイス
description: このトピックでは、X++ のインターフェイスについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150303
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8873876f3708c0b46b7c06ddae0a1d58f1aea502
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550846"
---
# <a name="x-interfaces"></a><span data-ttu-id="37d13-103">X++ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="37d13-103">X++ interfaces</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37d13-104">*インターフェイス* は、パブリック インスタンス メソッドのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="37d13-104">An *interface* specifies a set of public instance methods.</span></span> <span data-ttu-id="37d13-105">他から 1 つのクラスを派生させることなく、インターフェイスは無関係なクラス間の類似点を定義し適用します。</span><span class="sxs-lookup"><span data-stu-id="37d13-105">An interface defines and enforces similarities between unrelated classes without having to derive one class from the other.</span></span> <span data-ttu-id="37d13-106">**パブリック** キーワードをインターフェイス宣言の **インターフェイス** キーワードの前に明示的に追加しなくても、すべてのインターフェイスはパブリックになっています。</span><span class="sxs-lookup"><span data-stu-id="37d13-106">All interfaces are public, even if you don't explicitly add the **public** keyword in front of the **interface** keyword in interface declaration.</span></span> <span data-ttu-id="37d13-107">インターフェイス上のメソッドも公開されています。</span><span class="sxs-lookup"><span data-stu-id="37d13-107">The methods on an interface are also public.</span></span> <span data-ttu-id="37d13-108">**パブリック** というキーワードを明示的に含めることはオプションです。</span><span class="sxs-lookup"><span data-stu-id="37d13-108">Explicit inclusion of the keyword **public** is optional.</span></span> <span data-ttu-id="37d13-109">インターフェイスを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="37d13-109">To create an interface, follow these steps.</span></span>

1.  <span data-ttu-id="37d13-110">サーバー エクスプローラーで、プロジェクトを右クリックしてから**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37d13-110">In Server Explorer, right-click the project, and then click **Add**.</span></span>
2.  <span data-ttu-id="37d13-111">**新しい項目**ダイアログ ボックスで、**インターフェイス**を選択してからインターフェイスの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="37d13-111">In the **New Item** dialog box, select **Interface**, and then enter a name for the interface.</span></span>
3.  <span data-ttu-id="37d13-112">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37d13-112">Click **Add**.</span></span>

<span data-ttu-id="37d13-113">クラス宣言に **実装** キーワードを追加するとき、そのクラスは、インターフェイスによって指定されるメソッドを宣言し定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d13-113">When you add the **implements** keyword on a class declaration, the class must declare and define the methods that are specified by the interface.</span></span> <span data-ttu-id="37d13-114">クラス宣言では、複数のインターフェイスを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="37d13-114">A class declaration can implement multiple interfaces.</span></span> <span data-ttu-id="37d13-115">**実装** キーワードが単一で発生した後にインターフェイスを一覧表示し、インターフェイス名をコンマで区切ります。</span><span class="sxs-lookup"><span data-stu-id="37d13-115">List the interfaces after the single occurrence of the **implements** keyword, and separate the interface names by using commas.</span></span> <span data-ttu-id="37d13-116">クラスが実装するすべてのインターフェイス メソッドは、**パブリック** として明示的に宣言される必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d13-116">All interface methods that a class implements must be explicitly declared as **public**.</span></span> <span data-ttu-id="37d13-117">インターフェイスを実装するクラスも**パブリック**として宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37d13-117">A class that implements an interface must also be declared as **public**.</span></span> <span data-ttu-id="37d13-118">インターフェイスを**拡張**キーワードを使用して別のインターフェイスに拡張できます。</span><span class="sxs-lookup"><span data-stu-id="37d13-118">An interface can extend another interface by using the **extends** keyword.</span></span> <span data-ttu-id="37d13-119">ただし、インターフェイスは、複数のインターフェイスを拡張することはできません。</span><span class="sxs-lookup"><span data-stu-id="37d13-119">However, an interface can't extend more than one interface.</span></span>

<span data-ttu-id="37d13-120">通例として、インターフェイスの名前は `I` で始めます。</span><span class="sxs-lookup"><span data-stu-id="37d13-120">It is customary to preface the name of an interface with `I`.</span></span>

## <a name="interface-example"></a><span data-ttu-id="37d13-121">インターフェイスの例</span><span class="sxs-lookup"><span data-stu-id="37d13-121">Interface example</span></span>

<span data-ttu-id="37d13-122">次のコード例では、**自動車** クラスが **IDrivable** インターフェイスを実装しています。</span><span class="sxs-lookup"><span data-stu-id="37d13-122">In the following code example, the **Automobile** class implements the **IDrivable** interface.</span></span> <span data-ttu-id="37d13-123">**is** キーワードは、あるクラスがインターフェイスを実装するかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="37d13-123">The **is** keyword tests whether a class implements an interface.</span></span>

```X++
interface IDrivable
{
    int getSpeed()
    {
    }

    void setSpeed(int newSpeed)
    {
    }
}

class Automobile implements IDrivable
{
    int speed;

    public int getSpeed()
    {
        return speed;
    }

    public void setSpeed(int newSpeed)
    {
        speed = newSpeed;
    }
}

class UseAnAutomobile
{
    void DriveAutomobile()
    {
        IDrivable drivable;
        Automobile myAutomobile = new Automobile();
        str temp;

        myAutomobile = new Automobile();

        if (myAutomobile is IDrivable)
        {
            drivable = myAutomobile;
            drivable.setSpeed(42);
            temp = int2str(drivable.getSpeed());
        }
        else
        {
            temp = "Instance is not an IDrivable.";
        }

        info(temp);
    }
}
```
