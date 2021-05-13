---
title: X++ インターフェイス
description: このトピックでは、X++ のインターフェイスについて説明します。
author: RobinARH
ms.date: 06/17/2019
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150303
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2aff15ba1b965a3663aa292f9b2ab990f486a2f0
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866316"
---
# <a name="x-interfaces"></a><span data-ttu-id="f4265-103">X++ インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f4265-103">X++ interfaces</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4265-104">*インターフェイス* は、パブリック インスタンス メソッドのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="f4265-104">An *interface* specifies a set of public instance methods.</span></span> <span data-ttu-id="f4265-105">他から 1 つのクラスを派生させることなく、インターフェイスは無関係なクラス間の類似点を定義し適用します。</span><span class="sxs-lookup"><span data-stu-id="f4265-105">An interface defines and enforces similarities between unrelated classes without having to derive one class from the other.</span></span> 

<span data-ttu-id="f4265-106">**パブリック** キーワードをインターフェイス宣言の **インターフェイス** キーワードの前に明示的に追加しなくても、すべてのインターフェイスはパブリックになっています。</span><span class="sxs-lookup"><span data-stu-id="f4265-106">All interfaces are public, even if you don't explicitly add the **public** keyword in front of the **interface** keyword in interface declaration.</span></span> <span data-ttu-id="f4265-107">インターフェイス上のメソッドも公開されています。</span><span class="sxs-lookup"><span data-stu-id="f4265-107">The methods on an interface are also public.</span></span> <span data-ttu-id="f4265-108">**パブリック** というキーワードを明示的に含めることはオプションです。</span><span class="sxs-lookup"><span data-stu-id="f4265-108">Explicit inclusion of the keyword **public** is optional.</span></span> 

<span data-ttu-id="f4265-109">インターフェイスを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f4265-109">To create an interface, follow these steps.</span></span>

1.  <span data-ttu-id="f4265-110">サーバー エクスプローラーで、プロジェクトを右クリックしてから **追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4265-110">In Server Explorer, right-click the project, and then click **Add**.</span></span>
2.  <span data-ttu-id="f4265-111">**新しい項目** ダイアログ ボックスで、**インターフェイス** を選択してからインターフェイスの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4265-111">In the **New Item** dialog box, select **Interface**, and then enter a name for the interface.</span></span>
3.  <span data-ttu-id="f4265-112">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4265-112">Click **Add**.</span></span>

<span data-ttu-id="f4265-113">クラス宣言に **実装** キーワードを追加するとき、そのクラスは、インターフェイスによって指定されるメソッドを宣言し定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4265-113">When you add the **implements** keyword on a class declaration, the class must declare and define the methods that are specified by the interface.</span></span> <span data-ttu-id="f4265-114">クラス宣言では、複数のインターフェイスを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="f4265-114">A class declaration can implement multiple interfaces.</span></span> <span data-ttu-id="f4265-115">**実装** キーワードが単一で発生した後にインターフェイスを一覧表示し、インターフェイス名をコンマで区切ります。</span><span class="sxs-lookup"><span data-stu-id="f4265-115">List the interfaces after the single occurrence of the **implements** keyword, and separate the interface names by using commas.</span></span> 

<span data-ttu-id="f4265-116">クラスが実装するすべてのインターフェイス メソッドは、**パブリック** として明示的に宣言される必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4265-116">All interface methods that a class implements must be explicitly declared as **public**.</span></span> <span data-ttu-id="f4265-117">インターフェイスを実装するクラスも **パブリック** として宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4265-117">A class that implements an interface must also be declared as **public**.</span></span> <span data-ttu-id="f4265-118">インターフェイスを **拡張** キーワードを使用して別のインターフェイスに拡張できますが、ただし、インターフェイスは、複数のインターフェイスを拡張することはできません。</span><span class="sxs-lookup"><span data-stu-id="f4265-118">An interface can extend another interface by using the **extends** keyword, however, an interface can't extend more than one interface.</span></span>

<span data-ttu-id="f4265-119">通例として、インターフェイスの名前は `I` で始めます。</span><span class="sxs-lookup"><span data-stu-id="f4265-119">It is customary to preface the name of an interface with `I`.</span></span>

## <a name="interface-example"></a><span data-ttu-id="f4265-120">インターフェイスの例</span><span class="sxs-lookup"><span data-stu-id="f4265-120">Interface example</span></span>

<span data-ttu-id="f4265-121">次のコード例では、**自動車** クラスが **IDrivable** インターフェイスを実装しています。</span><span class="sxs-lookup"><span data-stu-id="f4265-121">In the following code example, the **Automobile** class implements the **IDrivable** interface.</span></span> <span data-ttu-id="f4265-122">**is** キーワードは、あるクラスがインターフェイスを実装するかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="f4265-122">The **is** keyword tests whether a class implements an interface.</span></span>

```xpp
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]