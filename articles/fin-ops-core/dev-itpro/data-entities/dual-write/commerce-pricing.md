---
title: Dynamics 365 Sales で Dynamics 365 Commerce 価格決定エンジンを使用する
description: このトピックでは、Microsoft Dynamics 365 Commerce 価格決定エンジンを使用して、Dynamics 365 Sales に売上の見積書を作成する方法について説明します。
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: 70282eb7856ae6b37e885eac2daf49efd971087d7c204af4b653263edb0d8fc4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716073"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Dynamics 365 Sales で Dynamics 365 Commerce 価格決定エンジンを使用する

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce 価格決定エンジンを使用して、Dynamics 365 Sales に売上の見積書を作成する方法について説明します。

Dynamics 365 Commerce 価格設定エンジンは、店舗レベルの価格設定、提携ベースの価格設定、ロイヤルティ ベースの価格設定、組み合わせ割引、数量割引、しきい値割引など、ほとんどの B2C (企業と一般消費者) 価格設定のシナリオに対応しています。 価格決定エンジンでは、複雑なルールを使用して、特定の見積または注文に対して最適な価格を決定します。

[デュアル書き込み](./dual-write-overview.md)を使用する場合は、価格決定のニーズに対して 3 つのオプションがあります。 この静的な価格決定は、Dynamics 365 Sales の価格表、Dynamics 365 Supply Chain Management の価格決定エンジン、または Dynamics 365 Commerce の価格決定エンジンを使用して行うことができます。 これらのオプションの中でも、 Commerce の価格設定エンジンは B2C シナリオに最適です。

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Sales で Commerce の価格設定エンジンを使用する

> [!NOTE]
> 現在、Commerce の価格決定エンジンは、販売での見積の作成にのみ使用できます。 Commerce の価格決定エンジンと販売注文の統合は、まだ使用できません。

ユーザーが Sales で販売見積を開始すると、デュアル書き込みフレームワークによって、見積の詳細が Commerce にコピーされます。 既存の見積明細行に対する変更や、Salesで新たに追加された見積明細行は、Commerce にコピーされます。 ユーザーは、Commerce の価格決定エンジンを使用して見積に価格を指定する際に、**価格見積り** を選択して Commerce の価格決定エンジンに基づいて見積の価格を更新できます。 価格は、Sales と Commerce の両方で自動的に更新されます。

## <a name="prerequisites"></a>必要条件

- Commerce の価格エンジンを Sales で使用するには、事前に [デュアル書き込みにおける見込顧客から売上へのプロセス](./dual-write-prospect-to-cash.md) の手順を実行しておく必要があります。
- 以下の手順で、手動入力の売買契約評価をオフにする必要があります。

    1. Commerce 環境で、**売掛金勘定 \> 設定 \> 売掛金勘定パラメーター** に移動します。
    1. **価格** タブの **売買契約評価**  クイックタブで、**手動入力** のチェックボックスをオフにし ます。

## <a name="additional-resources"></a>追加リソース

[二重書き込みの見込顧客を現金化](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]