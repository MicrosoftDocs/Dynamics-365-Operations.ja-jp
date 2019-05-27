---
title: ユーザーが Attract または Onboard の人員ピッカーで見つからない
description: このトピックでは、社内テナントのユーザーが Dynamics 365 for Talent Attract または Onboard アプリケーションの人員ピッカーに表示されない場合の対処方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518454"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Azure Active Directory ユーザーが人員ピッカーで見つからない

[!include [banner](includes/banner.md)]

## <a name="issue"></a>出庫

テナント用 Microsoft Azure Active Directory (Azure AD) で特定の有効なユーザーが、Dynamics 365 for Talent Attract または Onboard アプリケーションの人員ピッカーで名前を検索する際に表示されません。

## <a name="cause"></a>原因

特定のユーザー タイプは、現在 Attract および Onboard アプリケーションでサポートされていません。 ユーザーが Azure AD 企業間 (B2B) ゲスト ユーザーではないことを確認します。 「ユーザー タイプ」の情報は、Azure ポータルの Azure Active Directory ブレードにあります。

Azure B2B の詳細については、[Azure Active Directory B2B のゲスト ユーザー アクセスとは](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b)を参照してください。

B2B 以外のユーザーの場合、**ユーザー** オブジェクトに未完了の「ユーザー タイプ」プロパティを持つ可能性のある特定のユーザーがいます。 これは、Azure AD Powershell モジュールを使用して検証および修正できます。 詳細については、「[Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0)」を参照してください。

## <a name="resolution"></a>解像度

この問題を解決するにあたり次の手順を実行するために、Azure Active Directory テナントの「グローバル管理者」のアクセス許可または **User.ReadWrite.All** のアクセス許可が必要です。

影響を受けるユーザーの「ユーザー タイプ」を確認します。

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
コマンドは次の情報を返します。
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
ユーザーの **UserType** プロパティに注意してください。 **UserType** が空白、たとえば「メンバー」もしくは「ゲスト」ではない場合、次のコマンドを使用して **UserType** を更新してください。

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
