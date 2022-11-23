---
title: B2C テナントを Commerce に 設定
description: この記事では、Microsoft Dynamics 365 Commerce のユーザー サイト認証のために Azure Active Directory (Azure AD) の企業と顧客間 (B2C) テナントを設定する方法について説明します。
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785143"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>B2C テナントを Commerce に 設定

[!include [banner](includes/banner.md)]

この記事では、Dynamics 365 Commerce のユーザー サイト認証のために Azure Active Directory (Azure AD) の企業と顧客間 (B2C) テナントを設定する方法について説明します。

Dynamics 365 Commerce は Azure AD B2C を使用して、ユーザーの資格情報と認証フローをサポートします。 ユーザーは、これらのフローを使用して、登録、サインイン、およびパスワードのリセットを行うことができます。 Azure AD B2C では、ユーザー名やパスワードなどの機密性の高いユーザー認証情報を保存します。 B2C テナントのユーザー レコードには、B2C ローカル アカウント レコードまたは B2C ソーシャル ID プロバイダー レコードのいずれかが保存されます。 これらの B2C レコードは、Commerce 環境内の顧客レコードにリンクされます。

> [!WARNING] 
> Azure AD B2C は、2021 年 8 月 1 日までに古い (レガシ) ユーザー フローを破棄します。 したがって、ユーザー フローを新しい推奨バージョンに移行する必要があります。 新しいバージョンでは、機能パリティと新しい機能が提供されます。 推奨される B2C ユーザー フローには、Commerce のバージョン 10.0.15 以上のモジュール ライブラリを使用する必要があります。 詳細については、[Azure Active Directory B2C のユーザー フロー](/azure/active-directory-b2c/user-flow-overview) を参照してください。
 
 > [!NOTE]
 > Commerce 評価環境には、デモ用に Azure AD B2C テナントがプリロードされています。 評価環境では、次の手順を使用して独自の Azure AD B2C テナントを読み込む必要はありません。

> [!TIP]
> Azure AD ID 保護および条件付きアクセスにより、サイト ユーザーをさらに保護し、Azure AD B2C テナントのセキュリティを強化できます。 Azure AD B2C Premium P1 テナントおよび Premium P2 テナントが利用できる機能を確認するには、[Azure AD B2C の ID 保護と条件付きアクセス](/azure/active-directory-b2c/conditional-access-identity-protection-overview) を参照してください。

## <a name="dynamics-environment-prerequisites"></a>Dynamics 環境の前提条件

始める前に、次の前提条件を満たすことによって、Dynamics 365 Commerce 環境と e コマース チャネルが適切に構成されていることを確認してください。

- POS 操作の **AllowHtnymousAccess** の値を Commerce Headquarters で "1" に設定します。
    1. **POS 操作** に移動します。
    1. 操作グリッドで右クリックし、**パーソナライズ** を選択します。
    1. **フィールドを追加** を選択します。
    1. 使用可能な列の一覧で **AllowAnonymousAccess** 列を選択して追加します。
    1. **更新プログラム** を選択します。
    1. **612** の "顧客の追加" 操作の場合は、**AllowAnonymousAccess** を "1" に変更します。
    1. **1090 (レジスター)** ジョブを実行します。
- Commerce 本社で、番号順序の顧客勘定の **手動** 属性を **いいえ** に設定します。
    1. **小売とコマース \> 本社の設定 \> パラメーター \> 売掛金勘定パラメーター** の順に移動します。
    1. **番号順序** を選択します。
    1. **顧客勘定** 行で、**番号順序コード** 値をダブルクリックします。
    1. 番号順序の **一般** クイック タブで、**手動** を **いいえ** に設定します。

Dynamics 365 Commerce 環境を配置した後で、環境内の [シード データを初期化](enable-configure-retail-functionality.md) することもお勧めします。

## <a name="next-steps"></a>次のステップ

Commerce で B2C テナントを設定するプロセスを続行するには、[Azure ポータルで既存の Azure AD B2C テナントを作成またはリンクする](create-link-aad-b2c-tenant.md) に進みます。

## <a name="additional-resources"></a>追加リソース

[Azure ポータルでの既存の Azure AD B2C テナントを作成またはリンクする](create-link-aad-b2c-tenant.md)

[B2C アプリケーションを作成する](create-b2c-app.md)

[ユーザー フロー ポリシーの作成](create-user-flow-policies.md)

[ソーシャル ID プロバイダーの追加 (オプション)](add-social-identity-providers.md)

[新しい Azure AD B2C 情報で Commerce headquarters を更新する](update-hq-aad-b2c-info.md)

[コマース サイト ビルダーでの B2C テナントのコンフィギュレーション](config-b2c-tenant-site-builder.md)

[B2C 追加情報](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
