---
title: 新規ユーザーの作成
description: ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88d3f1fba05d944e78e4595018d190c3dc41e076
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907914"
---
# <a name="create-new-users"></a>新規ユーザーの作成

[!include [banner](../../includes/banner.md)]

Finance and Operations アプリにアクセスするには、まず **ユーザー** ページ (**システム管理 \> ユーザー \> ユーザー**) に追加する必要があります。 ユーザーには、組織の内部従業員、または外部顧客や仕入先が含まれます。 ユーザーは手動でインポートまたは追加できます。 すべてのユーザーは、準拠して使用するために正しいライセンスを取得する必要があります。

Finance and Operations アプリの購入方法とライセンスの取得方法については、[Microsoft Dynamics 365 ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409) を参照してください。

## <a name="assign-a-license-to-a-user"></a>ライセンスのユーザーへの割り当て
システム管理者は、[Microsoft 365 管理者センター](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)で、[ユーザーにライセンスを割り当てる](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)ことができます。

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Azure AD への外部ユーザーの追加とライセンスの割り当て 
外部ユーザーがライセンスを割り当てできるよう、テナント ディレクトリ (Azure Active Directory (Azure AD)) に表示される必要があります。 それら外部ユーザーは、ゲスト ユーザーとして Azure AD のテナントに追加した後、適切なライセンスを割り当てる必要があります。 Finance and Operations アプリの要件は、ゲスト ユーザーの会社が Azure AD を使用することです。 詳細については、[Azure ポータルで Azure Active Directory B2B コラボレーション ユーザーを追加する](/azure/active-directory/b2b/add-users-administrator) を参照してください。

## <a name="import-new-users-from-azure-ad"></a>Azure AD からの新規ユーザーのインポート 
1. **システム管理** \> **ユーザー** \> **ユーザー** の順に移動します。
2. アクション ウィンドウで、**ユーザーのインポート** を選択します。
3. インポートされるユーザーを選択します。 この一覧には、現在この環境のユーザーではない Azure AD ユーザーが含まれています。
4. **ユーザーのインポート** を選択します。
5. **閉じる** を選択します。

> [!NOTE]
> **会社** フィールドの値は、管理者の現在のセッション会社に基づいて設定されます。インポート後に、必要に応じロールと組織を割り当てる必要があります。 詳細については、[ユーザーのセキュリティ ロールへの割り当て](assign-users-security-roles.md) を参照してください。 条件付きで、ユーザーを **個人** に関連付けたり、言語などのユーザー オプションを更新したりする必要がある場合もあります。

## <a name="manually-add-a-new-user"></a>新規ユーザーを手動で追加
1. **システム管理** \> **ユーザー** \> **ユーザー** の順に移動します。
2. アクション ウィンドウで、**新規** を選択します。
3. **ユーザー ID** フィールドに、ユーザーの固有 ID を入力します。   
4. **ユーザー名** フィールドに、ユーザー名を入力します。  
5. **プロバイダー** フィールドで:
 - 内部ユーザーについては、既定値を使用します。 例: https://sts.windows.net/ で始まる Azure AD テナント。  
 - Service-2-Service accounts アカウントなどの Azure AD 以外のユーザーの場合は、基本テキスト値を入力します。 例: NA。 この値は、有効な ID プロバイダ値が使用された場合にエラーが発生する可能性がある不正な認証呼び出しを回避するのに役立ちます。  
 - 外部ユーザーまたはゲスト ユーザーの場合は、Azure AD テナント名を https://sts.windows.net/ の後に追加します。
6. **電子メール** フィールドに、ユーザーの完全な電子メール/ユーザー プリンシパル名を入力します。  
7. **会社** フィールドで、ユーザーの既定の起動時に開く会社を選択します。 
8. **保存** を選択します。

ユーザー レコードを保存すると、ID プロバイダーとテレメトリ ID の値が [Microsoft Graph](/graph/overview) 呼び出しに基づいて更新されます。 テレメトリ ID は、Azure AD のオブジェクト ID/セキュリティ識別子 (SID) に基づきます。

> [!NOTE]
> ユーザーを追加した後で、必要に応じロールと組織を割り当てる必要があります。 詳細については、[ユーザーのセキュリティ ロールへの割り当て](assign-users-security-roles.md) を参照してください。 条件付きで、ユーザーを **個人** に関連付けたり、言語などの **ユーザー オプション** を更新したりする必要がある場合もあります。

## <a name="change-a-user-id"></a>ユーザー ID の変更
ユーザー ID を変更するには、データベース内のキーの名前を変更する必要があります。 この手順を使用してユーザー ID を変更すると、すべての関連するユーザー設定が変更され、新しいユーザー ID を使用します。 たとえば、**SysLastValue** テーブルの使用状況情報は、新しいユーザー ID を参照するために更新されます。

> [!NOTE]
> ユーザー ID は、ユーザー情報テーブルの主キーです。 主キーへのすべての参照もデータベースで更新されるため、既存のユーザーが主キーの名前を変更するには時間がかかる場合があります。 

1. **システム管理 \> ユーザー \> ユーザー** の順に移動します。
2. 一覧でユーザーを選択し、**オプション\> レコード情報** を選択します。
3. **名前の変更** を選択します。
4. ユーザー ID に新しい固有の値を入力し、**OK** を選択します。 
5. **はい** を選択して確認します。

## <a name="additional-resources"></a>追加リソース

B2B ユーザーを実装するための詳細なオプションについては、[B2B ユーザーの Azure AD へのエクスポート](../implement-b2b.md) を参照してください。

コンフィギュレーション済システム アカウントの詳細については、[コンフィギュレーション済みのシステム アカウント](../pre-configured-system-accounts.md) を参照してください


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]