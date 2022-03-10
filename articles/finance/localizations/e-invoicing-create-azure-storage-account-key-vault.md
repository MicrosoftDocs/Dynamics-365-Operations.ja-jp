---
title: Azure ストレージ アカウントとキー コンテナーの作成
description: このトピックでは、Azure ストレージ アカウントとキー コンテナーを作成する方法について説明します。
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23fec7a00d800719e1a7d2c90f9d0977d56be038
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463860"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Azure ストレージ アカウントとキー コンテナーの作成

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>必要条件

このトピックのタスクを完了する前に、以下の前提条件を完了していることを確認してください :

- Azure でのキー コンテナーのリソースの作成。 詳細については、[Azure のキー コンテナー](/azure/key-vault/general/overview)を参照してください。
- Azure ストレージ アカウント (Blob ストレージ) の作成。 詳細については、[Azure ストレージ アカウントを管理する](/azure/storage/blobs/) を参照してください。

## <a name="overview"></a>概要

このトピックでは、2 つの主要な手順について説明します :

- Azure のストレージ アカウントを設定してストレージ アカウントの URI を取得します。
- キーコンテナーを設定し、ストレージ アカウントの URI を格納します。

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Azure のストレージ アカウントを設定してストレージ アカウントの URI を取得する

1. 電子請求に使用する予定のストレージ アカウントを開きます。
2. **データ ストレージ** > **コンテナー** に移動し、新しいコンテナーを作成します。
3. コンテナーの名前を入力し、**パブリック アクセス レベル** フィールドを **プライベート (匿名アクセスなし)** に設定し ます。
4. コンテナーを開き、**設定** > **アクセス ポリシー** に移動します。
5. **ポリシーの追加** を選択して、保存されているアクセス ポリシーを追加します。
6. 必要に応じて、 **識別子** フィールドと **アクセス許可** フィールドを設定します。 **キーのアクセス許可** フィールドで、すべてのアクセス許可を選択します。

    ![Blob ストレージのアクセス許可を付与します。](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. 開始日と有効期限を入力します。 有効期限は未来の日付にする必要があります。
8. **OK** をクリックしてポリシーを保存し、変更をコンテナーに保存します。
9. **設定** > **共有アクセス トークン** に移動し、フィールドの値を設定します。 
10. 開始日と終了日を入力します。 終了日は未来の日付にする必要があります。
11. **アクセス許可** フィールドで、次のアクセス許可を選択します: **読み取り**、**追加**、**作成**、**書き込み**、**削除**、および **一覧**。 
12. **SAS トークンと URL の生成** を選択します。
13. 値をコピーして、**Blob SAS URL** フィールドに保存します。 この値は、次の手順で使用され、*共有アクセス署名 URI* として参照されます。

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>キー コンテナーを設定し、ストレージ アカウントの URI を格納する

1. 電子請求に使用する Key Vault を開きます。
2. **設定** \> **秘密** に移動し、**生成/インポート** を選択して 新しい秘密を作成します。
3. **シークレットを作成** ページの **アップロード オプション** フィールドで、**手動** を選択します。
4. 秘密の名称を入力します。 この名前は、Regulatory Configuration Services (RCS) のサービス設定時に使用され、*キー コンテナーの秘密名称* と呼ばれます。
5. **値** フィールドに前の手順でコピーした共有アクセス署名 URI を入力し、**作成** を選択します。
6. アクセス ポリシーを設定して、作成したシークレットへの正しいレベルのセキュアなアクセスを電子請求に付与します。 **設定 \>アクセス ポリシー** に移動し 、**アクセス ポリシーの追加** を選択します。
7. **取得** と **一覧** の操作に、秘密のアクセス許可を設定します。

    ![サービス アクセスを付与します。](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. **取得** と **一覧** の操作に、証明書のアクセス許可を設定します。

    ![証明書のアクセス許可を付与します。](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. **プリンシパルの選択** フィールドで、**選択なし** を選択します。
10. **プリンシパル** ダイアログ ボックスで、**電子請求書サービス** を追加してプリンシパルを選択します。
11. **追加** を選択してから、**保存** を選択します。
12. **概要** ページで、 キー コンテナーの **DNS 名** の値をコピーして保存します。 この値は、RCS におけるサービスの設定時に使用され、*キー コンテナーの URI* として参照されます。

> [!NOTE]
> ストレージ アカウントのセキュリティを追加するには、Azure Defender For Storage を構成します。
> 
> 詳細については、[Azure Defender for Storage の概要](/azure/security-center/defender-for-storage-introduction) を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
