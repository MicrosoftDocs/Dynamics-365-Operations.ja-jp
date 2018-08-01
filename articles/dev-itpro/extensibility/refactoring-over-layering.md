---
title: "モデル制限を緩和し、拡張機能へのオーバーレイのリファクタリングを有効化する"
description: "このトピックでは、モデル制限の緩和と、拡張機能へのオーバーレイのリファクタリングの有効化に関する情報を提供します。 これは、モデルが Microsoft Dynamics 365 for Finance and Operations 8.0 でシールされているために必要です。"
author: CGarty
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: CGarty
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c3e31a6420c503093c55dfb6589b58a8aaf2326b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="relax-model-restrictions-to-enable-the-refactoring-of-over-layering-into-extensions"></a>モデル制限を緩和し、拡張機能へのオーバーレイのリファクタリングを有効化する

[!include [banner](../includes/banner.md)]

Dynamics 365 for Finance and Operations 8.0 およびこれ以降のすべてのリリースでは、オーバーレイを使用して Microsoft のコードをカスタマイズすることはできません。 代わりに、変更および動作を追加するため拡張機能が使用される必要があります。 「超過レイヤーなし」制限は、クラウド ERP サービスが顧客に提供するのに対する製品の発展の重要な部分です。それはすべての顧客が最新機能および最新修正の益を得られるよう、簡単に更新でき常に利用可能な最新バージョンを実行しています。

コードを 8.0 以降にアップグレードすると、コンパイルの際にオーバーレイをまだ使用するカスタマイズにエラーが発生します。 コードをリファクターするには、オーバーレイされているモデルのモデル記述子ファイルで、オーバーレイ制限を一時的に緩和することができます。 この一時的な緩和は、開発環境およびデモ環境でのみ機能し、スタンダード承認テスト (またはそれ以上) のサンドボックス環境や実稼動環境などのランタイム環境には配置できません。 記述子制限を緩和すると、拡張機能に徐々にリファクタリングされ、コンパイルされ、実行され、およびテストされるコードが有効になります。 

## <a name="detailed-process"></a>詳細なプロセス
モデル制限を緩和するには、次の手順を実行します。 クラウド環境またはローカル仮想マシン (VM) では、この手順を実行することができます。

1. Finance and Operations 8.0 開発環境向けに Dynamics 365 を導入します。 
2. ソリューションをアップグレードするには、Lifecycle Services (LCS) コード アップグレード サービスを実行します。
3. コンパイルを有効にするための必要に応じて Microsoft モデルでオーバーレイを一時的に許可します。
    
    a. C:\AOSService\PackagesLocalDirectory フォルダー内で目的のモデルを検索します。
    
    b. 記述子フォルダに移動します。 たとえば、\Currency\Descriptor です。
    
    c. XML ファイルを開きます。 たとえば、Currency.xml です。
    
    d. **AllowAndWarn** を示す **AxModelInfo** メタデータ要素内に**カスタマイズ**メタデータ要素を追加すると、ファイルの先頭は次のようになります。
            
    ```xml
    <AxModelInfo xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
    <AppliedUpdates xmlns:d2p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" />
    <Customization>AllowAndWarn</Customization>
    ```
    
4. 拡張機能へのオーバーレイのリファクタリングおよびテスト。 オーバーレイを解消するための拡張機能を利用します。 必要な場合は、拡張機能の要求を行います。
5. Microsoft モデルへの一時的な変更を元に戻します。 オーバーレイを使用するモデルの展開はできなくなるため、記述子ファイルを更新することが重要です。
 
## <a name="prototyping-extensibility-requests"></a>プロトタイプ拡張機能の要求
拡張子に向けてソリューションが段階的に移行する際、ソリューションを解除するための拡張性要求が必要とされる場所があります。 ソリューションのブロックを解除し、拡張機能への移行プロセスをスムーズにするために必要なものを完全に理解するために、拡張機能を別のモデルでプロトタイプ化することができます。

1. いくつかのオーバーレイをリファクターする拡張機能の必要性を識別します。
2. 拡張機能のプロトタイプを拡張プロトタイプ モデルに追加します。

   - 列挙の拡張機能のために、列挙のコピーを拡張プロトタイプ モデルに入れ、それを拡張可能としてマークします。
    
   - メソッド抽出の拡張機能のために、拡張プロトタイプ モデルで、抽出されたメソッドとオーバーレイされたオリジナルを作成します。
    
3. プロトタイプの拡張機能を使用します。
4. プロトタイプの拡張機能が不十分な場合は、対応する要求を作成します。
5. 拡張機能がプラットフォームまたはアプリケーションに実装されている場合、プロトタイプ拡張機能およびそれに関連するオーバーレイを拡張プロトタイプ モデルから削除する必要があります。
6. 拡張機能にリファクタリングされたすべてのオーバーレイがソリューションにあり、拡張プロトタイプ モデルが空白になると、ソリューション リファクタリングは完了します。

