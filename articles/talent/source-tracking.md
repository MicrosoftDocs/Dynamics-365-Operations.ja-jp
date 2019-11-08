---
title: 候補者のプロファイルおよび応募のソースの追跡
description: このトピックでは、候補者のプロファイルおよびアプリケーションのソースの追跡に関する情報を提供します。
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 5b368e97a716cd1ce4f668c2a97326877a2d3dff
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551890"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a>候補者のプロファイルおよび応募のソースの追跡

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> このトピックに記載されている機能は、プレビュー レビュー リリースの一部として、対象とするユーザーが使用可能です。 コンテンツおよび機能は、変更されることがあります。 この機能を使用するには、Attract の**管理者設定**を使用して有効にするよう管理者に依頼してください。 将来のリリースでは、ソース追跡レポートを提供します。 詳細については、[Talent のプレビュー機能の利用](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature) を参照してください。

候補者が職務に応募すると、Attract は自動的に申請のソースを追跡し、採用活動に役立つ貴重な情報を提供します。 採用担当者および採用マネージャーは、職務または人材プールに候補者を手動で追加するときに、アプリケーション ソースを選択できます。

アプリケーション ソースは、**活動**タブ下のアプリケーション活動の詳細、および人材プールの**プロファイル**で利用可能なアプリケーション履歴を確認できます。 アプリケーションおよび人材プールの**プロファイル**タブの候補者の詳細から、候補者のプロファイルソースを検索できます。

> [!NOTE] 
> プロセス テンプレートについては、[包括採用アドオン](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) を参照してください。

## <a name="pre-configured-sources"></a>構成済みのソース

既定のソース リストには、一般的なアプリケーションソースが含まれています。 **職務ボード**および**ソーシャル ネットワーク**のような、一部のソース タイプには追加のソースの詳細があります。 たとえば、**ソーシャル ネットワーク**には Facebook および Twitter が含まれます。 **照会**ソース タイプでは、参照先として内部従業員を指定することができます。 既定のソース リストには、次の構成済みのソースが含まれます。

-   Attract キャリア サイト

-   代理店

-   キャリアフェア

-   会社のマーケティング

-   会議 & 取引の表示

-   職務協会

-   職務ボード

    -   Indeed

    -   Seek

    -   CareerBuilder

    -   Google Jobs

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   雑誌 & 出版物

-   ソーシャル ネットワーク

    -   Facebook

    -   Twitter

-   大学の採用

-   LinkedIn

-   分類

-   照会

-   採用担当者が追加

-   外

## <a name="customize-the-source-list"></a>ソース リストをカスタマイズする 

追加のアプリケーション ソースを含めるようにソース リストを拡張することができます。 リストをカスタマイズするには、[Attract のオプション セットの拡張する](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract) の手順に従います。 追加のソース含めるために **TalentSource** エンティティを編集する。 

ユーザー インターフェイス (UI) への悪影響を回避するため、以下の場合、**TalentCategory** 列挙値（名前ではない）を編集または削除しないでください。

- **照会**
- **LinkedIn**
- **外**

代わりに、他のタイプのソースを追加するために **TalentSource** 列挙を拡張できます。
