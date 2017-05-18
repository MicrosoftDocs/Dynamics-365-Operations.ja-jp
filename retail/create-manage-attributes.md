---
title: "属性の作成と管理"
description: "この記事は、Microsoft Dynamics 365 for Operations の属性について説明します。 [属性] により、ユーザー定義フィールドを使用して製品およびその特性を説明できます。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: a5c45bb0b9ed10c989a3222a751df3f454b14a0b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/26/2017


---

# <a name="create-and-manage-attributes"></a>属性の作成と管理

[!include[banner](includes/banner.md)]


この記事は、Microsoft Dynamics 365 for Operations の属性について説明します。 [属性] により、ユーザー定義フィールドを使用して製品およびその特性を説明できます。

[属性] により、ユーザー定義フィールドを使用して製品およびその特性を説明できます。 たとえば、製品のメモリ サイズとハード ディスク能力を指定できます。製品が [エネルギー スター] に準拠しているかどうかを示します。 属性は、製品カテゴリ、小売チャンネルなどのさまざまな小売エンティティに関連付けられており、それらに対して既定値を設定できます。 製品は、製品カテゴリまたは小売チャンネルに関連付けられる場合、それらの属性および属性の既定値を継承します。 既定値は、個々の製品レベルや小売チャンネル レベル、または小売カタログで上書きできます。

#### <a name="examples"></a>例

| カテゴリ   | 属性                | 許容値          | 既定値 |
|------------|--------------------------|-----------------------------|---------------|
| テレビ & ビデオ | ブランド                    | [ブランド] の有効な値       | なし          |
| テレビ         | スクリーン サイズ              | 20″–80″                     | なし          |
| テレビ         | [垂直解像度]      | 480i、720p、1080i、または 1080p | 1080p         |
| テレビ         | 画面の更新頻度      | 60hz、120hz、または 240hz       | 60hz          |
| テレビ         | [HDMI 入力]              | 0–10                        | 3             |
| テレビ         | [DVI 入力]               | 0–10                        | 1             |
| テレビ         | [複合の入力]         | 0–10                        | 2             |
| テレビ         | [コンポーネントの入力]         | 0–10                        | 1             |
| LCD        | [3D 準備完了]                 | 要否                   | 有           |
| LCD        | [3D 有効]               | 要否                   | 無            |
| プラズマ     | [作業開始の温度]      | 32–110 度              | 32            |
| プラズマ     | [作業終了の温度]        | 32–110 度              | 100           |
| プロジェクション | プロジェクションの管の保証 | 6、12、または 18 か月         | 12            |
| プロジェクション | # プロジェクションの管の     | 1–5                         | 3             |


## <a name="attribute-type"></a>属性タイプ
  [![attributes-fixed-copy](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) 
  
属性は、属性タイプをベースにしています。 属性タイプは、特定の属性に入力できるデータのタイプを識別します。 現在、Microsoft Dynamics 365 for Operations では、次の属性タイプをサポートしています :

-   [**通貨**] – この属性タイプは、通貨の値をサポートします。 これはバインドできますし (値の範囲をサポートできる) 開いたままにもできます。
-   [**日時**] – この属性タイプは、日付と時刻の値をサポートします。 これはバインドできますし (値の範囲をサポートできる) 開いたままにもできます。
-   [**小数点**] – この属性タイプは、小数点以下を含む数値をサポートします。 また、測定単位もサポートします。 これはバインドできますし、(値の範囲をサポートできる) 開いたままにもできます。
-   [**整数**] – この属性タイプは、数値の値をサポートします。 また、測定単位もサポートします。 これはバインドできますし (値の範囲をサポートできる) 開いたままにもできます。
-   [**テキスト**] – この属性タイプは、テキストの値をサポートします。 また、事前定義された一連の使用可能な値 (列挙型) がサポートされます。
-   **ブール値** – この属性タイプは、バイナリ値をサポートします (**true**/**false**)。
-   [**参照**]

## <a name="attribute"></a>属性
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) 名前、フレンドリ名、説明、ヘルプ テキストに加えて、次の情報のうち 1 つ以上を属性にキャプチャすることができます :

-   既定値
-   属性の検索、絞り込み、並べ替えができるかどうかを示すメタデータなどの属性メタデータ

## <a name="attribute-group"></a>属性グループ
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) 属性が定義されると、属性グループにグループ化できます。 属性グループは、個々の属性のグループを提供し、小売カテゴリまたは小売チャンネルに割り当てることができます。

## <a name="assigning-attribute-groups-to-retail-categories"></a>小売カテゴリへの属性グループの割り当て
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) 1 つ以上の属性グループを小売製品カテゴリ階層のカテゴリ ノードに関連付けることができます。 製品を分類されている場合、属性グループに含まれる属性を継承します。

## <a name="assigning-attribute-groups-to-retail-stores"></a>小売店舗への属性グループの割り当て
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) 1 つ以上の属性グループを小売店舗階層の 1 つ以上の小売店舗に関連付けることができます。 製品が特定の小売店舗に対して強化されている場合、属性グループに含まれる属性を継承します。

## <a name="overriding-attribute-values"></a>属性値の上書き
### <a name="at-the-product-level"></a>製品レベルで

  [![createandmanageattribute-14-1024x576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) 属性の既定値を製品レベルで上書きできます (個々の製品にに対して)。

### <a name="in-a-retail-catalog"></a>小売カタログで

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) 属性の既定値を、特定の小売チャンネルを対象とする特定のカタログの個々の製品に対して上書きできます。

### <a name="at-the-retail-channel-level"></a>小売チャネル レベルで

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) 属性の既定値を、特定の小売チャンネルを対象とする特定のカタログの個々の製品に対して上書きできます。




