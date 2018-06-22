---
title: "Project Service Automation の統合パラメーター"
description: "Project Service Automation を Dynamics 365 for Finance and Operations と統合する場合に、データを既定にする方法をコンフィギュレーションできます。"
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Project Service Automation の統合パラメーター

**Project Service Automation の統合パラメーター** ページで、Project Service Automation を Finance and Operations と統合する場合、データを既定にする方法をコンフィギュレーションできます。 Finance and Operations の Project Service Automation から正常にプロジェクトが同期されるために次の事柄が設定される必要があります。

> [!NOTE]
> プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。




| **タブ**                      | **フィールド**                          | **説明**                    |
|------------------------------|------------------------------------|--------------------------------|
| **一般**                  | **既定のプロジェクト タイプ**               | 統合テンプレートの既定値が提供されていない場合、Project Service Automation からプロジェクトが同期されるときに**プロジェクト タイプ**の既定を選択します。 同期中に、新しいプロジェクトに含まれる**プロジェクト タイプ**はこの値に設定され、Project Service Automation からプロジェクト契約明細行が同期されるときに更新できます。               |
| **一般**                  | **時間カテゴリ**                      | 時間見積が Project Service Automation から同期される場合に、**時間カテゴリ**の既定値を選択します。 同期時に、時間見積および時間の実績が Project Service Automation から同期されている場合、Finance and Operations の新しいプロジェクトの時間予測に含まれている**カテゴリ**はこの値に設定されます。   |
| **一般**                  | **手数料カテゴリ**                       | 手数料の実績が Project Service Automation から同期される場合に、**手数料カテゴリ**の既定値を選択します。 同期時に、手数料の実績が Project Service Automation から同期されている場合、Finance and Operations の新しい手数料トランザクションに含まれている**カテゴリ**はこの値に設定されます。          |
| **プロジェクト グループの既定値**   | **プロジェクト タイプ** | 既定のプロジェクト グループを設定するプロジェクト タイプを選択できる行を追加するには、**新規**をクリックします。 特定のプロジェクト タイプは、コンフィギュレーションで 1 回のみ選択できます。              
|                              | **プロジェクト グループ**          | 指定したプロジェクト タイプの既定のプロジェクト グループを選択します。 新しいプロジェクトが Project Service Automation から同期されるときに、統合テンプレートの既定値が提供されていない場合、**プロジェクト グループ**はプロジェクト タイプに基づいて既定になります。  |
| **請求タイプの既定値**    | **請求タイプ** | **新規**をクリックして行を追加し、既定の明細行プロパティを設定する請求タイプを選択します。 特定の請求タイプは、コンフィギュレーションで 1 回のみ選択できます。          |
|                              | **明細行プロパティ**| 指定した請求タイプの既定の明細行プロパティを選択します。 新しい時間見積、新しい経費見積、または新しい実績が Project Service Automation から同期されるときに、**明細行プロパティ**は請求タイプに基づいて既定になります。          |
| **機能ロック**    |                   | Project Service Automation から作成されたプロジェクトおよび契約の Finance and Operations で無効にする機能を選択します。 たとえば、契約およびプロジェクトを編集し、作業分解構造を作成し、Finance and Operations でタイムシートを入力する機能を無効にすることができます。 パラメーター設定によって利用できない場合でも、会計関連のフィールドは継続して有効になります。 既定では、すべての機能が有効になります。           |

