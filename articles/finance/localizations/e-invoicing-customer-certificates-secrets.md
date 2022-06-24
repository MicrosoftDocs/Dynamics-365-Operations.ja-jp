---
title: 顧客の証明書とシークレット
description: この記事では、電子請求で顧客の証明書とシークレットを設定する方法について説明します。
author: dkalyuzh
ms.date: 02/07/2022
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
ms.openlocfilehash: a4d33135bf352a4c4a245e597e0c3c7467317864
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880663"
---
# <a name="customer-certificates-and-secrets"></a>顧客の証明書とシークレット

[!include [banner](../includes/banner.md)]

既に Regulatory Configuration Service (RCS) に Microsoft Azure Key Vault 参照がある場合は、Key Vault の証明書およびシークレットへの参照を作成できます。 Key Vault 参照がまだない場合は、作成方法について [サービス環境](e-invoicing-service-environments.md) を参照してください。

## <a name="create-certificates-and-secrets"></a>証明書とシークレットの作成

証明書とシークレットを作成および設定するには、次の手順に従います。

1. RCS アカウントにサインインします。
2. **グローバリゼーション機能** ワークスペースの **環境t** セクションで、**電子請求** タイルを選択します。
3. **環境の設定** ページのアクション ペインで、**サービス環境** を選択します。
4. **サービス環境** ページのアクション ペインで、**Key Vault パラメーター** を選択します。
5. **Key Vault パラメーター** ページで Key Vault 参照を選択してから、**証明書** セクションで **追加** を選択します。
6. **名称** フィールドに、Key Vault 証明書またはシークレットの名前を入力します。 詳細については、[Azure ポータルで Azure ストレージ アカウントを作成する](e-invoicing-create-azure-storage-account-azure-portal.md) を参照してください。
7. **説明** フィールドに説明を入力します。
8. キー コンテナーに格納されている証明書を参照する場合は、**タイプ** フィールドで **証明書** を選択します。 キー コンテナーに格納されているシークレットを参照する場合は、**シークレット** を選択します。
9. **保存** を選択します。

> [!NOTE]
> 一部のシナリオでは、.cer ファイル名拡張子を持つ公開証明書を使用する必要があります。 ただし、Key Vault では、このタイプの証明書を Key Vault 証明書としてインポートおよび保存することはサポートされていません。 これらのシナリオでは、.cer ファイルを Base-64-encoded X.509 (.CER) 文字列として保存する必要があります。 次に、Key Vault シークレットで、ファイル内の **BEGIN CERTIFICATE** 行と **END CERTIFICATE** 行の間に表示される文字列を格納します。 サービス環境では、Key Vault レコードへの参照を作成し、**タイプ** フィールドを **証明書** に設定する必要があります。

## <a name="create-a-chain-of-certificates"></a>一連の証明書の作成

国/地域固有の請求書で、デジタル署名を適用するか、外部 Web サービスへの安全な (Secure Sockets Layer \[SSL\]) 接続を確立するために一連の証明書が必要な場合は、証明書が次の順序である一連の証明書を作成します。

1. ルート証明書
2. 中間証明書
3. エンド ユーザー証明書

ルート証明機関 (CA) は、証明書の信頼できるソースです。 中間 CA 証明書は、エンド ユーザー証明書とルート CA 証明書をリンクするブリッジです。

一連の証明書を作成および設定するには、次の手順に従います。

1. **Key Vault パラメーター** ページのアクション ペインで、**一連の証明書** を選択します。
2. **新規** を選択して、一連の証明書を作成します。
3. **名称** フィールドに、一連の証明書の名前を入力します。
4. **説明** フィールドに説明を入力します。
5. **証明書** セクションで、**追加** を択してチェーンに証明書を追加します。
6. **上** ボタン、または **下** ボタンを使用して、証明書チェーンの位置を変更します。 一覧の一番上に CA ルート証明書を、一番下にエンド ユーザー証明書を配置します。
7. **保存** を選択します。

必要な数の Key Vault 参照を RCS に作成することができます。 ストレージの Shared Access Signature (SAS) トークンのシークレットは、指定されたサービス環境を Key Vault 参照にリンクするために使用されることに注意してください。 サービス環境の設定時に使用するストレージ SAS トークンのシークレットも含まれるキー コンテナーに格納されている Key Vault 証明書とシークレットを参照できます。
