---
title: 実行予定
description: このトピックでは、資産管理の実行予定について説明します。
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fae899bcfa8bb2566d1a9aee3f0dbe22bc219edf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825641"
---
# <a name="scheduled-execution"></a>実行予定

[!include [banner](../../includes/banner.md)]

 

ワーク オーダーのサービス レベルを使用して、実行予定を設定できます。 (ワーク オーダーのサービス レベルの詳細については、[サービス レベルおよび説明](service-level-and-description.md)を参照してください。) 実行予定により、メンテナンス作業者の作業計画に柔軟性がもたらされます。これは、ワーク オーダーを完了する間隔について、より詳細な要件または詳細度の低い要件を設定できるためです。 たとえば、生産施設で予定よりも早く作業を完了するメンテナンス作業者は、現在の週に計画されていますが、当日とは限らない別の近い作業に進むことができます。 このアプローチでは、作業者の計画とジョブの完了を最適化できます。

ワーク オーダーに関連する実行予定の設定は、汎用または固有にすることができます。 特定のワーク オーダー タイプ、資産タイプなどに限定されない汎用の明細行を設定できます。 または、特定のワーク オーダー タイプ、資産タイプ、メンテナンス作業タイプに適用される実行予定の明細行を作成することもできます。

1. **資産管理** \> **設定** \> **ワーク オーダー** \> **実行予定** を選択します。
2. **新規** を選択して、実行予定明細行を作成します。
3. **機能的な場所**、**ワーク オーダー タイプ**、**資産タイプ**、**メーカー**、**モデル**、**メンテナンス作業タイプ カテゴリ**、**メンテナンス作業タイプ**、**メンテナンス作業タイプ バリアント**、および **取引** のフィールドで、必要に応じて値を選択します。
4. **サービス レベル** フィールドで、ワーク オーダーのサービス レベルを選択します。 このフィールドを空白のままにした場合は、最も一般的なタイプの実行予定明細行を作成します。 一般的な明細行の例については、次の図の最初のレコードを参照してください。 この明細行によって、ワーク オーダーのサービス レベルのないすべてのワーク オーダーを、特定の日時に対してスケジュールできるようになります。
5. **実行予定** フィールドで、時間間隔を選択します。
6. **保存** を選択します。

![実行予定](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]