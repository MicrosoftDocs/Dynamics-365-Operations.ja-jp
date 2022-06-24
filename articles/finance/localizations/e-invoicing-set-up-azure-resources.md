---
title: 電子請求のための Azure リソースの設定
description: この記事では、電子請求用の Microsoft Azure リソースを設定するプロセスの概要を説明します。
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c5b7b2ca4d7733fb1c75ded8798655699284fe1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907732"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>電子請求のための Azure リソースの設定

[!include [banner](../includes/banner.md)]

電子請求用の Microsoft Azure リソースを設定するプロセスには 3 つの手順があります。 最初の 2 つの手順 "Azure ポータルで Azure Key Vault を作成する" と "Azure ポータルで Azure ストレージ アカウントを作成する" は必須です。 3 番目の "SharePoint 接続を構成する" はオプションです。

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Azure ポータルで Azure Key Vault を作成する

ご利用の Azure サブスクリプションでキー コンテナーを作成します。 電子請求用に別のキー コンテナーを作成し、他のアプリケーションとシークレットを結合しないことをお勧めします。 電子ドキュメントでのシナリオに必要な数のシークレットと証明書を作成します。 次の手順で作成する Azure ストレージ アカウントの Shared Access Signature (SAS) トークンを保存するには、少なくとも 1 つのシークレットを作成する必要があります。

この手順の完了方法の詳細については、[Azure ポータルで Azure Key Vault を作成する](e-invoicing-create-azure-key-vault-azure-portal.md) を参照してください。

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Azure ポータルで Azure ストレージ アカウントを作成する

電子請求サービスによって生成された電子ドキュメントおよびファイルをすべて所有するか、サービスを入力します。 これらのドキュメントとファイルは、Azure サブスクリプションで作成した Azure ストレージ アカウントに格納されます。 本サービスは、Key Vault シークレットから取得した SAS トークンを使用してストレージ アカウントにアクセスします。

この手順の完了方法の詳細については、[Azure ポータルで Azure ストレージ アカウントを作成する](e-invoicing-create-azure-storage-account-azure-portal.md) を参照してください。

## <a name="configure-a-sharepoint-connection"></a>SharePoint 接続の構成

場合によっては、電子ファイルを SharePoint に保存して、SharePoint から取得する必要があります。 電子請求サービスが SharePoint フォルダーにアクセスできるようにするには、SharePoint へのアクセスを構成します。

この手順を完了する方法については、[SharePoint 接続を構成する](e-invoicing-create-sharepoint-connection.md) を参照してください。
