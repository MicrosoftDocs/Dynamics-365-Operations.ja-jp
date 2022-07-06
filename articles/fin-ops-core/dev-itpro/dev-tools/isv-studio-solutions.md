---
title: ISV Studio を使用した ISV パッケージからの X++ モジュールのリンク
description: この記事では、ISV Studio を使用した X++ パッケージのリンクについて説明します。
author: jorisdg
ms.date: 04/08/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: 70381
ms.assetid: 90ae4ae6-f19a-4ea5-8bd9-1d45729b0636
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebe71e0714d60c0abc2d5aa41fcedc568b06d50b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867045"
---
# <a name="link-x-modules-from-isv-packages-by-using-isv-studio"></a>ISV Studio を使用した ISV パッケージからの X++ モジュールのリンク

独立系ソフトウェア ベンダー (ISVs) は、[Microsoft Power Platform ISV Studio](/powerapps/developer/data-platform/isv-app-management) を使用して、X++モジュールを登録済みの製品およびソリューションにリンクできます。 リンクにより、ISV は財務と運用アプリでのアプリケーションの成功と使用を監視できます。

> [!NOTE]
> X++ から ISV Studio へのリンクが正常に機能するには、顧客がすべての ISV モデルに正しいソリューション ID を持つ ISV パッケージを配置している必要があります。 また、顧客の環境はバージョン 10.0.16 以上である必要があります。

## <a name="find-the-product-id-in-microsoft-partner-center"></a>Microsoft パートナー センターで製品 ID を検索する

パートナー センターにサインインし、製品の **オファーの概要** ページを開きます。 次の例に示すように、ブラウザの URL バーから製品 ID グローバル一意識別子 (GUID) を検索します。

```HTTP
https://partner.microsoft.com/dashboard/commercial-marketplace/offers/<product-ID-GUID>/overview
```

> [!NOTE]
> 製品 ID 製品のオファー コードと一致するとは限りませんが、類似している場合があります。 記述子でオファー コードを使用しても、ISV Studio に対して X++ モジュールを正しく識別できません。

## <a name="update-your-x-model-descriptors"></a>X++ モデル記述子の更新

ソリューションを構成するすべてのモデルについて、記述子 XML ファイルを検索します。 ソリューションに属しているすべての記述子で、パートナー センターの製品 ID を使用して `SolutionId` タグを更新します。 予期される結果を取得するには、要素の順序が次の例と一致している必要があります。

:::code language="xml" source="code/descriptor.xml" highlight="19,20":::

再コンパイル後、X++ バイナリには製品 ID が含まれ、Tier 2+ サンドボックスまたは運用環境に配置された後に ISV Studio にリンクされます。
