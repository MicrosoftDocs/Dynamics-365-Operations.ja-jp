---
title: Azure ポータルで Azure ストレージ アカウントを作成する
description: この記事では、電子請求書の Azure ストレージ アカウントを作成する方法について説明します。
author: dkalyuzh
ms.date: 02/14/2022
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
ms.openlocfilehash: 4380261140086bcb278162f8dc70b39eaa7078fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898021"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Azure ポータルで Azure ストレージ アカウントを作成する

[!include [banner](../includes/banner.md)]

電子請求サービスが生成したすべての電子ファイル、または処理中にサービスへ移動したすべての電子ファイルは、Microsoft Azure ストレージ アカウント コンテナーに保存されます。 電子請求がこのコンテナーにアクセスできるようするには、ストレージ アカウントの Shared Access Signature (SAS) トークンを電子請求サービスに提供する必要があります。 また、トークンが安全に保存されるのを確認するために、SAS トークンを直接提供しないでください。 代わりに、トークンを Azure キー コンテナーに保存し、Azure Key Vault シークレットを提供します。

1. 電子請求サービスで使用するストレージ アカウントを開きます。
2. **設定** \> **構成** の順に移動し、**Blob のパブリック アクセスを許可する** パラメーターが **有効** に設定されているかを確認してください。
3. **データ ストレージ** \> **コンテナー** に移動し、新しいコンテナーを作成します。
4. コンテナーの名前を入力し、**パブリック アクセス レベル** フィールドを **プライベート (匿名アクセスなし)** に設定し ます。
5. 新しいコンテナーを開き、**設定** \> **アクセス ポリシー** に移動します。
6. **ポリシーの追加** を選択して、保存されているアクセス ポリシーを追加します。
7. 必要に応じて **識別子** フィールドを設定します。
8. **アクセス許可** フィールドで、すべてのアクセス許可を選択します。

    !["ポリシーの追加" ダイアログ ボックスの "アクセス許可" フィールドで選択されたアクセス許可すべて。](media/e-invoicing-azure-1.png)

9. 開始日と終了日を入力します。 終了日は未来の日付にする必要があります。
10. **OK** をクリックしてポリシーを保存し、変更をコンテナーに保存します。
11. **設定** \> **共有アクセス トークン** に移動し、フィールドの値を設定します。
12. 開始日と終了日を入力します。 終了日は未来の日付にする必要があります。
13. **アクセス許可** フィールドで、次のいずれかのアクセス許可を選択します。

    - 既読
    - 追加
    - 作成
    - 書き込み
    - 消去
    - リスト

14. **SAS トークンと URL の生成** を選択します。
15. 値をコピーして、**Blob SAS URL** フィールドに保存します。 この値は、この手順で後ほど使用され、*共有アクセス署名 URI* として参照されます。
16. 電子請求に使用する Key Vault を開きます。
17. **設定** \> **シークレット** に移動し、**生成/インポート** を選択して新しいシークレットを作成します。
18. **シークレットを作成** ページの **アップロード オプション** フィールドで、**手動** を選択します。
19. 秘密の名称を入力します。 この名前は、Regulatory Configuration Service (RCS) のサービス設定時に使用され、*キー コンテナーのシークレット名* と呼ばれます。 RCS の設定方法に関する詳細については、[Regulatory Configuration Service (RCS) の設定](e-invoicing-set-up-rcs.md) を参照してください。
20. **値** フィールドに、前述の手順でコピーした Shared Access Signature URI を入力します。
21. **作成** を選択します。
