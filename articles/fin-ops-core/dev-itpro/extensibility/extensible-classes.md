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
ms.openlocfilehash: 778eb4e07273262ab99d9c3c3147dfe0f03d774a
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367014"
---
# <a name="write-extensible-classes"></a>拡張可能クラスの書き込み

[!include [banner](../includes/banner.md)]

クラスとそのメソッドには、単一の責任が必要です。 長期的な変更に耐えるクラスをデザインするために以下の点に留意してください。 クラスに必要なもの:

+ 明確な目的
+ 適切な名前 (クラス名およびメソッド名)
+ 拡張する必要があるメソッドのみ拡張性のために公開されます。つまり、主要なルールは、できる限り拡張を最小限にすることです。
    - すべてのパブリックおよび保護メソッドが X++ における拡張性ポイントとなります。 新しいメソッドを導入するたびに、ダウンストリーム ユーザーはメソッドに追加のロジックを挿入する新しい方法を取得します。

### <a name="example"></a>例

**拡張不可コード**

```xpp
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

**拡張可能コード**

```xpp
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

## <a name="class-hierarchies"></a>クラス階層
出荷時のパターンを使用できる新規または既存のクラス階層の場合、SysExtension フレームワークにより簡単に拡張可能になります。 これらの拡張は完全に切り離されるため、基本クラスに変更を加えなくても新しいサブクラスを追加することができます。 したがってより少ないコードが必要です。 さらに、コストラクトのコントラクトが変わらないので、パブリック アプリケーション プログラミング インターフェイス (API) への変更はありません。 したがって、リファクタリングは低リスクです。
    
いくつかの既存のファクトリ メソッドは、インスタンス コンストラクターを使用してサブクラスをインスタンス化しない可能性があります。 代わりに、**コンストラクト**などの静的コンストラクターを呼び出すことができます。 これらのファクトリ メソッドに SysExtension フレームワークが使用される場合、重大な変更が発生します。サブクラスの静的コンストラクターが呼び出されなくなるためです。 このような場合は、既定のケースにのみ SysExtension フレームワークを使用します。
    
クラス階層構造の詳細については、次のブログ記事を参照してください。

+ [SysExtension フレームワーク – 問題発生時](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/sysextension-framework-to-the-rescue)
+ [Dynamics 365 for Finance and Operations への拡張機能のご要望の採用 #2 - SysExtension フレームワーク](https://community.dynamics.com/ax/b/axinthefield/posts/embrace-the-extensions-mindset-with-dynamics-365-for-finance-and-operations-2-sysextension-framework)

## <a name="deprecation"></a>廃止
クラスまたはパブリックまたは保護メソッドが不要になった場合、必ずまず警告を使用し、メソッドが廃止されたことをユーザーに通知します。 次に、すべてのユーザーは、変更または新しい API を取り込むことができ、メソッドを廃止できます。 クラスおよびメソッドの廃止 (または、それ以外の場合はクラス メンバーの削除) は、大きな変更点です。 詳細については、[重大な変更](breaking-changes.md)を参照してください。
