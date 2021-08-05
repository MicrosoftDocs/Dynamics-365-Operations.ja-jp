---
title: X++ インターフェイス
description: このトピックでは、X++ のインターフェイスについて説明します。
author: RobinARH
ms.date: 06/17/2019
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e601582623291433943dbc4d200a9782e4221907
ms.sourcegitcommit: ff5e892a91a1585472af2191ae45d6291cceb7f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2021
ms.locfileid: "6661352"
---
# <a name="x-interfaces"></a>X++ インターフェイス

[!include [banner](../includes/banner.md)]

*インターフェイス* は、パブリック インスタンス メソッドのセットを指定します。 他から 1 つのクラスを派生させることなく、インターフェイスは無関係なクラス間の類似点を定義し適用します。 

**パブリック** キーワードをインターフェイス宣言の **インターフェイス** キーワードの前に明示的に追加しなくても、すべてのインターフェイスはパブリックになっています。 インターフェイス上のメソッドも公開されています。 **パブリック** というキーワードを明示的に含めることはオプションです。 

インターフェイスを作成するには、次の手順を実行します。

1.  サーバー エクスプローラーで、プロジェクトを右クリックしてから **追加** をクリックします。
2.  **新しい項目** ダイアログ ボックスで、**インターフェイス** を選択してからインターフェイスの名前を入力します。
3.  **追加** をクリックします。

クラス宣言に **実装** キーワードを追加するとき、そのクラスは、インターフェイスによって指定されるメソッドを宣言し定義する必要があります。 クラス宣言では、複数のインターフェイスを実装することができます。 **実装** キーワードが単一で発生した後にインターフェイスを一覧表示し、インターフェイス名をコンマで区切ります。 

クラスが実装するすべてのインターフェイス メソッドは、**パブリック** として明示的に宣言される必要があります。 インターフェイスを実装するクラスも **パブリック** として宣言する必要があります。 インターフェイスを **拡張** キーワードを使用して別のインターフェイスに拡張できますが、ただし、インターフェイスは、複数のインターフェイスを拡張することはできません。

通例として、インターフェイスの名前は `I` で始めます。

## <a name="interface-example"></a>インターフェイスの例

次のコード例では、**自動車** クラスが **IDrivable** インターフェイスを実装しています。 **is** キーワードは、あるクラスがインターフェイスを実装するかどうかをテストします。

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