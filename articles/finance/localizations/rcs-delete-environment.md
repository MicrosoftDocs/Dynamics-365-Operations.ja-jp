---
title: Regulatory Configuration Service (RCS) - RCS 環境の削除
description: この記事では、Regulatory Configuration Service (RCS) システム管理者が RCS 環境および関連データを削除する方法について説明します。
author: kfend
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, System Admin
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
ms.openlocfilehash: bdcb6820ead72fce0f89bf80cc5e474cb3942724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277243"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) - RCS 環境の削除

[!include [banner](../includes/banner.md)]

この記事では、Regulatory Configuration Service (RCS) システム管理者が RCS 環境および関連データを削除する方法について説明します。

この記事の手順を完了する前に、以下の前提条件を満たす必要があります:

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
