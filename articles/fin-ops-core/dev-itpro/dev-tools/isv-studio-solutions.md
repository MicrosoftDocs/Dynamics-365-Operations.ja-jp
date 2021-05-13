---
title: ISV Studio を使用して、独立系ソフトウェア ベンダー (ISV) パッケージから X++ モジュールをリンク
description: このトピックでは、ISV Studio を使用した X++ パッケージのリンクについて説明します。
author: jorisdg
ms.date: 04/08/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 70381
ms.assetid: 90ae4ae6-f19a-4ea5-8bd9-1d45729b0636
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9a6b4618a7184255ed6580805f8af35fbde0b8e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881895"
---
# <a name="link-x-modules-from-independent-software-vendor-isv-packages-by-using-isv-studio"></a>ISV Studio を使用して、独立系ソフトウェア ベンダー (ISV) パッケージから X++ モジュールをリンク

独立系ソフトウェア ベンダー (ISVs) は、[Microsoft Power Platform ISV Studio](https://docs.microsoft.com/powerapps/developer/data-platform/isv-app-management) を使用して、X++モジュールを登録済みの製品およびソリューションにリンクできます。 リンクにより、ISV は Finance and Operations アプリでのアプリケーションの成功と使用を監視できます。

> [!NOTE]
> X++ から ISV Studio へのリンクが正しく機能するには、顧客ははすべての ISV モデルに正しいソリューション ID を持つ ISV パッケージを展開している必要があり、顧客の環境はバージョン 10.0.16 以降を実行している必要があります。

## <a name="find-the-product-id-in-microsoft-partner-center"></a>Microsoft パートナー センターで製品 ID を検索する

パートナー センターにサインインし、製品の **オファーの概要** ページを開きます。 次の例に示すように、ブラウザの URL バーから製品 ID GUID (グローバル一意識別子) を検索します。

```HTTP
https://partner.microsoft.com/en-us/dashboard/commercial-marketplace/offers/<product-ID-GUID>/overview
```

> [!NOTE]
> 製品 ID 製品のオファー コードと一致するとは限りませんが、類似している場合があります。 記述子でオファー コードを使用しても、ISV Studio に対して X++ モジュールを正しく識別できません。

## <a name="update-your-x-model-descriptors"></a>X++ モデル記述子の更新

ソリューションを構成するすべてのモデルについて、記述子 XML ファイルを検索します。 ソリューションに属しているすべての記述子で、パートナー センターの製品 ID を使用して `SolutionId` タグを更新します。

```xml
<AxModelInfo xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
    <!-- XML content -->
    <SolutionId>product-ID-GUID</SolutionId>
</AxModelInfo>
```

再コンパイル後、X++ バイナリには製品 ID が含まれ、Tier2+ サンドボックスまたは実稼働環境に配置された後に ISV Studio にリンクされます。
