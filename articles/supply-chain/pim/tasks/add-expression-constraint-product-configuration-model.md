---
title: 製品コンフィギュレーション モデルへ式の制約の追加
description: この手順は、製品コンフィギュレーション モデルに新しい式の制約を追加する方法を表示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920884"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>製品コンフィギュレーション モデルへ式の制約の追加

[!include [banner](../../includes/banner.md)]

この手順は、製品コンフィギュレーション モデルに新しい式の制約を追加する方法を表示します。 ユーザーが金属の前グリルを選択した場合は、コーナーの保護をスピーカーに適用する必要があることを義務付ける方法を表示します。 その手順は、デモ会社 USMF で [ハイエンド スピーカー] コンポーネントを使用します。

## <a name="create-an-expression-constraint"></a>式の制約の作成

1. **製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。
3. 一覧で、目的のレコードを見つけ、選択します。
    * この例では、ハイエンド スピーカー モデルを使用します。  
4. 一覧で、選択した行のリンクを選択します。
5. **制約** セクションを展開します。
6. **追加** を選択します。
7. **作成** を選択します。
8. **名前** フィールドに値を入力します。

## <a name="enter-expression"></a>式の入力

1. **式の編集** を選択します。
    * この段階で、タスク記録のユーザー インターフェイスのロックを解除する場合、制約式の構築のため、IntelliSense と記号のリストを使用できます。  
2. **ConstraintBody** フィールドで、「Implies[FrontGrill=="Metal", CornerProtection] 」と入力します。
    * この式ロジックの状態 : [前グリル] が金属の場合、角の保護オプションを選択する必要があります。  
3. **検証** を選択します。
    * 検証機能は、制約式に対して実行され、構文エラーを確認します。  
4. **閉じる** を選択します。
5. **OK** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]