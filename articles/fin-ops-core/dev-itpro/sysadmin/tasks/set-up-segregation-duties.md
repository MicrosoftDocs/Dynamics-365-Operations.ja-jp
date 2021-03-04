---
title: 職務分掌の設定
description: 異なるユーザーが実行する必要があるタスクを分割するルールを設定できます。
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688176"
---
# <a name="set-up-segregation-of-duties"></a>職務分掌の設定

[!include [banner](../../includes/banner.md)]

異なるユーザーが実行する必要があるタスクを分割するルールを設定できます。 この概念は職務分掌と呼ばれます。 たとえば、同じ担当者が、商品受入の確認と仕入先への支払処理の両方を実施するのは望ましくない場合があります。 職務分掌により、不正のリスクを減らし、エラーや反則を検出できます。 職務分掌を使用して、内部管理ポリシーを適用することもできます。 ルールを作成するには、次の手順を完了します。 この手順を完了するには、システム管理者である必要があります。 この手順の作成に使用するデモ データの会社は DAT です。 

1. **ナビゲーション ウィンドウ > モジュール > システム管理 > セキュリティ > 職務分掌 > 職務分掌ルール** の順に移動します。
2. **新規** をクリックします。
3. **名前** フィールドに、ルールの値を入力します。
4. **最初の職務権限** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、目的のレコードを見つけ、選択します。 ルールによって制御される最初の職務を選択します。
6. **2 番目の職務権限** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。 
7. 一覧で、目的のレコードを見つけ、選択します。 ルールによって制御される 2 番目の職務を選択します。
10. **重要度** フィールドで、オプションを選択します。 同じユーザーまたはロールが両方の職務を実行するときに発生するリスクの重要度を選択します。  
11. **セキュリティ リスク** フィールドで、値を入力します。 セキュリティ リスクの説明を入力します。  
12. **セキュリティ対策** フィールドで、値を入力します。 セキュリティ リスクを軽減するために実行するアクションの説明を入力します。 たとえば、プロセスの詳細確認の実施、月次管理確認の実施、または他の部門とのリソースの共有により、リスクを軽減することができます。     
13. **保存** をクリックします。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]