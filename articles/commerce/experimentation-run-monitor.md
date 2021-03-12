---
title: 実験の実行と監視
description: このトピックでは、サードパーティ サービスで実験を実行および監視する方法について説明します。 また、実験開始後にバリエーションを変更する方法についても説明します。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ba6fb94033e227790e01676819308bb4f0cd6868
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965221"
---
# <a name="run-and-monitor-an-experiment"></a>実験の実行と監視

このトピックでは、サードパーティのアプリケーションで実験を実行および監視し、必要に応じてバリエーションを変更する方法について説明します。 このトピックの手順を完了する前に、Commerce の実験を [公開](experimentation-preview-publish.md) しておく必要があります。 

次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。 追加の手順については、個別のトピックで説明します。

[![実験ユーザー体験 - 実行と監視](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

バリエーションを公開すると、Commerce で実験を実行するために必要となるすべての手順が完了します。 次の手順では、ユーザーがページを要求したときに各ユーザーに表示するバリエーションを決定します。 サードパーティ サービスがその決定を行いますが、最初にサービス内で実験を有効にする必要があります。 実験を有効化する手順はサービスによって異なるため、サービスまたはプロバイダーに含まれている手順に従う必要があります。 実験が有効化されていない場合、ユーザーにはページの既定のバージョンのみが表示されます (バリエーションは表示されません)。

統計的に有効な結果を得るには、データを収集するのに十分な期間、実験を実行し続ける必要があります。 サードパーティ サービスを使用して、実験の実行中に実験関連のデータおよび分析を監視します。

## <a name="adjust-your-variations"></a>バリエーションの調整
何らかの理由でバリエーションを変更する必要がある場合は、次の手順を実行します。

> [!IMPORTANT]
> Commerce またはサードパーティ サービスの実際の実験に変更を加えた場合、その結果は大きな影響を受ける可能性があります。 実験でコースを実行し、大きな変更に対して新しい実験を作成することを検討してください。

1. Commerce のサイト ビルダーで **実験** を選択し、 対象の実験を選択します。 
1. ドロップダウン メニューから更新するバリエーションを選択します。
1. 必要な変更を加えた後、バリエーションをプレビューして公開します。 詳細については、[実験をプレビューして公開する](experimentation-preview-publish.md) を参照してください。
1. サードパーティ サービスに移動して、実験の設定に関連する変更を行います。
    
## <a name="previous-step"></a>前のステップ
[実験のプレビューと公開](experimentation-preview-publish.md)

## <a name="next-step"></a>次のステップ
[バリエーションのレベルを上げて実験を完了する](experimentation-review-complete.md)
