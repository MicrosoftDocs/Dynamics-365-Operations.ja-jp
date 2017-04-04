---
title: "個人スキルと業務ニーズの調整"
description: "作業者、申請者、または連絡担当者がロールを効果的に遂行するために必要なスキルを追跡できます。 また、特定のジョブに必要なスキルを指定できます。"
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 720a1f272948eb310dc3cd02588aeec40b556d20
ms.openlocfilehash: 31dda85ff2e4a4e5380401b031b2dd74acff394b
ms.lasthandoff: 03/31/2017


---

# <a name="align-workforce-skills-with-business-needs"></a>個人スキルと業務ニーズの調整

作業者、申請者、または連絡担当者がロールを効果的に遂行するために必要なスキルを追跡できます。 また、特定のジョブに必要なスキルを指定できます。

ユーザーが追跡できるスキルの例は次が含まれます:
-   監督 : 他の従業員の作業を監督する能力。
-   リーダーシップ : 従業員や業務を率いる能力。
-   計画 : 先を見通し、その展望を形作り、さらに、それを行動に移す能力。
-   HTML : HTML コードを記述する能力。

個人またはジョブへのスキル割り当て、スキル マッピング検索の作成、スキル プロファイルの作成の前に、**スキル** ページでスキルに関する情報を入力する必要があります。 各スキルに対して、スキル タイプおよび評価モデルを選択できます。

## <a name="rating-models"></a>評価モデル
評価モデルにより、従業員の実際のスキル レベル、達成に必要な作業レベル、ジョブに必要なスキルを評価できます。 評価モデルには、最大 10 個のレベルを入力できます。  評価モデルの各レベル係数が割り当てられます。  要素値が異なる評価モデルを使用するロットのスキルを正規化するのに使用されます。  係数は0-9必要と各レベルの数であるための係数が必要です。  レベルの係数の値が大きいほど、評価モデルで重要になります。

## <a name="specify-job-skills"></a>職務スキルの指定
ジョブに関する情報を入力すると、そのジョブに必要な作業を行う必要があります。従業員スキルを指定できます。  また、各スキルのためのスキルの重要性レベル望ましいレベルも指定できます。 同じスキルでも、職務によって要求される重要性レベルが異なる場合があります。

## <a name="enter-skills-for-workers-applicants-or-contacts"></a>作業者、申請者、または連絡担当者のスキルの入力
作業者、申請者、または連絡担当者の目標スキルまたは実際のスキルを入力できます。 目標スキルとは、その従業員が達成を計画しているスキルです。 実際のスキルとは、従業員が現在持っているスキルです。

## <a name="skill-mapping-and-skill-mapping-profiles"></a>スキル マッピングとスキル マッピング プロファイル
タスクの特定のタイプの実行に利用するため、申請者、または連絡担当者を検索するためのスキル マッピング検索を作成できます。 スキルをスキル マッピングにsearchesの表示、教育、証明書、要職に、プロジェクト経験は、入力した基準に一致する結果が返される。  たとえば、組織の労働災害が自分のCPAを利用できる把握すると便利であるかもしがあります。

スキル マッピング プロファイルは、業務ニーズに直接対応する資格の現在の従業員または連絡を検索することができます。  たとえば、組織の開職位のスキル マッピング プロファイルを作成できます。 特定のジョブのプロファイルを作成して、そのジョブからスキル、教育、証明書をコピーすることにより、プロファイルに入力される基準の 1 つ以上に一致する作業者、申請者、連絡担当者を簡単に検索できます。また、ジョブに要求されるスキルに最も適合する候補者を一覧表示できます。

<table>
<thead>
<tr class="header">
<th><strong>メモ </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>スキル マッピング検索に含めるよう選択した作業者、申請者、および連絡担当者のみを、スキル マッピングの結果一覧に表示したり、スキル プロファイルに含めることができます。 作業者、申請者、連絡担当者をスキル マッピング検索に含める場合は、次の各ページで、<strong>スキル マッピングの対象に含める</strong>の選択を [はい] に設定します。
<ul>
<li>ワーカー</li>
<li>従業員</li>
<li>申請者</li>
<li>連絡先</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a>スキル ギャップ分析およびスキル プロファイル分析
特定の日付における作業者、申請者、または連絡担当者のコンピテンシーの一覧を表示するスキル プロファイル分析を作成できます。 個人のスキルを特定のジョブに必要なスキルと比較するスキル ギャップ分析を作成できます。  



<a name="see-also"></a>参照
--------

[Human resources](index.md)


