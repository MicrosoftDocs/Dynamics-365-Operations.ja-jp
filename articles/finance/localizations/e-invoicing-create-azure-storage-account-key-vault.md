---
title: Azure ストレージ アカウントとキー コンテナーの作成
description: このトピックでは、Azure ストレージ アカウントとキー コンテナーを作成する方法について説明します。
author: gionoder
ms.date: 02/12/2021
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
ms.openlocfilehash: b7df4933c1373893e00f48ea3a21bd5af40719a9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840223"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>Azure ストレージ アカウントとキー コンテナーの作成

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>必要条件

このトピックのタスクを完了する前に、以下の前提条件を完了していることを確認してください :

- Azure でのキー コンテナーのリソースの作成。 詳細については、[Azure のキー コンテナー](https://docs.microsoft.com/azure/key-vault/general/overview)を参照してください。
- Azure ストレージ アカウント (Blob ストレージ) の作成。 詳細については、[Azure ストレージ アカウントを管理する](https://docs.microsoft.com/azure/storage/blobs/) を参照してください。

## <a name="overview"></a>概要

このトピックでは、2 つの主要な手順について説明します :

- Azure のストレージ アカウントを設定してストレージ アカウントの URI を取得します。
- キーコンテナーを設定し、ストレージ アカウントの URI を格納します。

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>Azure のストレージ アカウントを設定してストレージ アカウントの URI を取得する

1. 電子請求に使用する予定のストレージ アカウントを開きます。
2. **Blob サービス** \> **コンテナー** に移動 し、新しいコンテナーを作成します。
3. コンテナーの名前を入力し、**パブリック アクセス レベル** フィールドを **プライベート (匿名アクセスなし)** に設定し ます。
4. コンテナーを開き、 **設定 \> アクセス ポリシー** に移動します。
5. **ポリシーの追加** を選択して、保存されているアクセス ポリシーを追加します。
6. 必要に応じて、 **識別子** フィールドと **アクセス許可** フィールドを設定します。 **キーのアクセス許可** フィールドで、すべてのアクセス許可を選択します。

    ![Blob ストレージのアクセス許可を付与する](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. 開始日と有効期限を入力します。 有効期限は未来の日付にする必要があります。
8. **OK** をクリックしてポリシーを保存し、変更をコンテナーに保存します。
9. ストレージ アカウントに戻り、**記憶域エクスプローラー (プレビュー)** を開きます。
10. コンテナーを右クリックし、**共有アクセス署名の取得** を選択します。
11. **共有アクセス署名** ダイアログ ボックスで、**URI** フィールドに値をコピーして格納します。 この値は、次の手順で使用され、*共有アクセス署名 URI* として参照されます。

    ![URI 値の選択とコピー](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>キー コンテナーを設定し、ストレージ アカウントの URI を格納する

1. 電子請求に使用する Key Vault を開きます。
2. **設定** \> **秘密** に移動し、**生成/インポート** を選択して 新しい秘密を作成します。
3. **シークレットを作成** ページの **アップロード オプション** フィールドで、**手動** を選択します。
4. 秘密の名称を入力します。 この名前は、Regulatory Configuration Services (RCS) のサービス設定時に使用され、*キー コンテナーの秘密名称* と呼ばれます。
5. **値** フィールドで、**共有アクセス署名 URI** を選択し、**作成** を選択します。
6. アクセス ポリシーを設定して、作成したシークレットへの正しいレベルのセキュアなアクセスを電子請求に付与します。 **設定 \>アクセス ポリシー** に移動し 、**アクセス ポリシーの追加** を選択します。
7. **取得** と **一覧** の操作に、秘密のアクセス許可を設定します。

    ![サービス アクセスの付与](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. **取得** と **一覧** の操作に、証明書のアクセス許可を設定します。

    ![証明書のアクセス許可の付与](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. **プリンシパルの選択** フィールドで、**選択なし** を選択します。
10. **プリンシパル** ダイアログ ボックスで、**電子請求書サービス** を追加してプリンシパルを選択します。
11. **追加** を選択し、**キー コンテナーの変更を保存する** を選択します。
12. **概要** ページで、 キー コンテナーの **DNS 名** の値をコピーして保存します。 この値は、RCS におけるサービスの設定時に使用され、*キー コンテナーの URI* として参照されます。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

