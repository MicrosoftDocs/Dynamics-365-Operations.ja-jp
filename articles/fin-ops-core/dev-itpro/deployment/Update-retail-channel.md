---
title: Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用
description: このトピックでは、クラウドでホストされているコマース チャネル コンポーネントへの更新プログラムと拡張機能を適用する方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: d6b47b1ebfb7339d99d7913ebe3167321e8f0d88
ms.sourcegitcommit: abd1dd6cc00daee847480828d8a3ba567bc17714
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2021
ms.locfileid: "5117447"
---
# <a name="apply-updates-and-extensions-to-commerce-scale-unit-cloud"></a>Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用

[!include[banner](../includes/banner.md)]

アプリケーション バージョン 8.1.2 以降でレベル 2 サンドボックスまたは運用環境を更新し、Commerce Scale Unit (CSU) を初期化した場合は、チャネル コンポーネントも更新する必要があります。 このトピックでは、CSU に更新と拡張を適用する方法について説明します。

CSU の更新は累積的です。 つまり、適用する更新すべてに、以前のリリースされたすべての変更がが含まれます。 Dynamics 365 Commerce の拡張の配置可能パッケージを適用することも累積的なプロセスであり、拡張機能の以前に配置されたバージョンが置き換えられます。

## <a name="prerequisites"></a>必要条件

続行する前に、まず更新および拡張機能 (該当する場合) を環境に適用する必要があります。 詳細については、[クラウド環境への更新プログラムの適用](apply-deployable-package-system.md)を参照してください。

CSU を更新するには、それぞれについて、次の手順を実行します。

1. **環境の詳細** ページで、**環境機能 > Retail およびコマース** に移動します。
2. **コマース配置設定** ページで、**更新** を選択します。
3. 選択パネルで、更新先のバージョンを選択します。
4. 最新のサービス更新プログラムを適用して最新の機能にアクセスすることも、最新の品質更新プログラムに更新して、現在展開されているサービス更新プログラムの品質改善を適用することもできます。 詳細については、[Lifecycle Services (LCS) から更新プログラムをダウンロード](../migration-upgrade/download-hotfix-lcs.md) を参照してください。
5. また、同時に拡張機能を適用することもできます。 

拡張機能を CSU に適用するには、次の手順を実行します。

1. **コマース配置設定** ページで、**拡張機能の適用** を選択します。
2. 選択パネルで、適用する拡張機能を選択します。

> [!NOTE]
> LCS の **コマース配置設定ページ** でパッケージを展開する前に、まず Microsoft Dynamics Lifecycle Services (LCS) でコマース配置可能パッケージをプロジェクト資産ライブラリにアップロードしてください。

**更新プログラムの適用** および **拡張機能の適用** 操作の両方はダウンタイム (最大 1 時間) を伴い、場合によっては最大 2 時間以上になる場合があります。 たとえば、CSU の米国以外の場所を更新する場合、大量のデータ、または複雑なスキーマの更新が行われます。 ダウンタイム期間の現実的な予測については、運用環境で使用する予定のものと同等の更新およびデータセットに対するサンドボックス UAT のダウンタイム期間を記録します。 この時間中、次のことが発生します。

- クラウドでホストされている Commerce チャネルは機能しません (POS オフライン機能が有効な場合を除く)。
- オフライン機能が有効になっている POS デバイスの機能が制限されます。
- CCSU に依存しているすべての電子商取引クライアントが中断されます。
- CSU でホストされているチャネルも影響を受けません。
- 本社機能も影響を受けません。

> [!NOTE]
> 拡張機能と更新プログラムを同時に適用するには、1 回のダウンタイムが必要なため、複数のダウンタイムを避ける効果的な方法です。

## <a name="view-history"></a>履歴の表示
最新の操作履歴をスケールユニットで表示するには、**アクション** タブの **履歴** を選択し、**スケール ユニットの履歴** ページを開きます。 このページでは、初期化、サービス更新、品質更新、バージョン、拡張機能の詳細、その他の関連情報など、最近の操作を表示できます。

## <a name="csu-auto-update-sequence"></a>CSU の自動更新順序

> [!NOTE]
> CSUの自動更新は、徐々にすべてのコマース顧客に展開されます。 LCS プロジェクトの所有者または環境管理者である場合は、CSU の自動更新が LCS プロジェクトに展開されるときに、電子メールで通知されます。

CSU は、Microsoft によって自動更新された後、次の順序で実行されます。

![CSU の自動更新順序](./media/CSU-auto-update-timeline.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]