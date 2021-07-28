---
title: Regulatory Configuration Service (RCS) - RCS 環境の削除
description: このトピックでは、Regulatory Configuration Service (RCS) システム管理者が RCS 環境および関連データを削除する方法について説明します。
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: cf82abbe5493eac9665323738441fa016205e9ef
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355010"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) - RCS 環境の削除

[!include [banner](../includes/banner.md)]

このトピックでは、Regulatory Configuration Service (RCS) システム管理者が RCS 環境および関連データを削除する方法について説明します。

このトピックの手順を完了する前に、以下の前提条件を満たす必要があります:

- ユーザーには、RCS 環境の **システム管理者** ロールが割り当てられている必要があります。
- **システム管理者** ロールには **RCSDeleteEnvironmentDuty** ロールが割り当てられている必要があります。

## <a name="delete-an-rcs-environment"></a>RCS 環境の削除

1. RCS を開き、**電子申告** ワークスペース タイルを選択します。
2. **関連リンク** セクションで、**RCS 環境の削除** を選択します。

    ![関連リンク セクションで、RCS 環境リンクを削除する。](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. 表示されるダイアログ ボックスで、環境削除のスコープに関するメッセージを確認します。

    ![RCS 環境の削除ダイアログ ボックスのメッセージ。](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > RCS 環境の削除は取り消しできません。
    >
    > この操作により、選択した RCS 環境、およびグローバル リポジトリに格納されている機能やコンフィギュレーションを含む関連データが削除されます。 他の組織と共有する機能やコンフィギュレーションは共有解除され、依存関係がない場合は削除されます。 依存関係がある機能やコンフィギュレーションは、廃止としてマークされます。

4. 表示されるフィールドに、RCS 環境のグローバル一意識別子 (GUID) を入力して、削除することを確定します。 環境の GUID は削除メッセージに含まれます。
5. **環境の削除** を選択します。
    
これで、RCS 環境および関連データが削除されました。

> [!IMPORTANT]
> RCS 環境を削除した後に、データを復旧する方法はありません。 使用可能な任意の RCS 地域に、新しい RCS 環境を作成できます。
