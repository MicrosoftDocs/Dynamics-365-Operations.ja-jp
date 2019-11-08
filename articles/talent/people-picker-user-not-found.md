---
title: ユーザーが Attract または Onboard の人員ピッカーで見つからない
description: このトピックでは、社内テナントのユーザーが Dynamics 365 Talent - Attract または Onboard の人員ピッカーに表示されない場合の対処方法について説明します。
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
ms.openlocfilehash: d84dd9c22738a1b4fc5edb5331d4aa213b82facb
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551936"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a>ユーザーが Attract または Onboard の人員ピッカーで見つからない
[!include [banner](includes/banner.md)]

## <a name="issue"></a>問題点

テナント用 Microsoft Azure Active Directory (Azure AD) の特定ユーザーは、Dynamics 365 Talent: Attract または Dynamics 365 Talent: Onboard の人員ピッカーで名前を検索している際には表示されません。

## <a name="cause"></a>原因

特定のユーザー タイプは、現在 Attract および Onboard でサポートされていません。 ユーザーが Azure AD 企業間 (B2B) ゲスト ユーザーではないことを確認します。 「ユーザー タイプ」の情報は、Azure ポータルの Azure Active Directory ブレードにあります。

Azure B2B の詳細については、[Azure Active Directory B2B のゲスト ユーザー アクセスとは](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b)を参照してください。

B2B 以外のユーザーの場合、**ユーザー** オブジェクトに未完了の「ユーザー タイプ」プロパティを持つ可能性のある特定のユーザーがいます。 これは、Azure AD Powershell モジュールを使用して検証および修正できます。 詳細については、「[Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0)」を参照してください。

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
