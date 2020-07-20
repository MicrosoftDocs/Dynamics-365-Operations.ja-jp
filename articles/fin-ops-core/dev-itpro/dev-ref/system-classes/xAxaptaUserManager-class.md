---
title: xAxaptaUserManager クラス
description: このトピックでは、xAxaptaUserManager クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 195fe36d0ec0abd6d3c58ea5dcd6c1d5312f692d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502994"
---
# <a name="class-xaxaptausermanager"></a>クラス xAxaptaUserManager

[!include [banner](../../includes/banner.md)]

```xpp
class xAxaptaUserManager extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                               | 説明                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| public container enumerateDomains(str server)                                                        |                                                                        |
| public xAxaptaUserDetails enumerateDomainUsers(str domainName)                                       |                                                                        |
| public str generatePassword()                                                                        |                                                                        |
| public xAxaptaUserDetails getDomainUser(str domainName, str userLogin)                               |                                                                        |
| public str getFQDN(str domainName, \[boolean throwError\])                                           |                                                                        |
| public container getGroupsForUser(str userName)                                                      |                                                                        |
| public container getRolesForUser(str userName, str company)                                          | 特定のユーザーのロールを取得します。                                         |
| public xAxaptaUserDetails getSIDFromName(str userLogin, str domainName, UserAccountType accountType) | 特定のユーザー ログオン、ドメイン、および勘定タイプからのユーザーの詳細を取得します。 |
| public str getUserSid(str username, str domain)                                                      |                                                                        |
| public boolean validateDomain(str domain)                                                            |                                                                        |
| public boolean validateOrgUnit(str ouName)                                                           |                                                                        |
| public boolean validatePassword(str username, str domain, str password)                              |                                                                        |
| public boolean validateSecGroup(str secGroup)                                                        |                                                                        |
| public void new()                                                                                    | xAxaptaUserManager クラスの新しいインスタンスを初期化します。            |
| public void updateUserRoleAssignments(UserId userId, container roles, container removeRoles)         |                                                                        |
| public void finalize()                                                                               |                                                                        |

## <a name="method-enumeratedomains"></a>メソッド enumerateDomains

```xpp
public container enumerateDomains(str server)
```

### <a name="parameters---enumeratedomains"></a>パラメーター - enumerateDomains

server  

### <a name="return-value---enumeratedomains"></a>戻り値 - enumerateDomains

## <a name="method-enumeratedomainusers"></a>メソッド enumerateDomainUsers

```xpp
public xAxaptaUserDetails enumerateDomainUsers(str domainName)
```

### <a name="parameters---enumeratedomainusers"></a>パラメーター - enumerateDomainUsers

domainName  

### <a name="return-value---enumeratedomainusers"></a>戻り値 - enumerateDomainUsers

## <a name="method-generatepassword"></a>メソッド generatePassword

```xpp
public str generatePassword()
```

### <a name="return-value---generatepassword"></a>戻り値 - generatePassword

## <a name="method-getdomainuser"></a>メソッド getDomainUser

```xpp
public xAxaptaUserDetails getDomainUser(str domainName, str userLogin)
```

### <a name="parameters---getdomainuser"></a>パラメーター - getDomainUser

domainName  

<!-- -->

userLogin  

### <a name="return-value---getdomainuser"></a>戻り値 - getDomainUser

## <a name="method-getfqdn"></a>メソッド getFQDN

```xpp
public str getFQDN(str domainName, [boolean throwError])
```

### <a name="parameters---getfqdn"></a>パラメーター - getFQDN

domainName  

<!-- -->

throwError  

### <a name="return-value---getfqdn"></a>戻り値 - getFQDN

## <a name="method-getgroupsforuser"></a>メソッド getGroupsForUser

```xpp
public container getGroupsForUser(str userName)
```

### <a name="parameters---getgroupsforuser"></a>パラメーター - getGroupsForUser

userName  

### <a name="return-value---getgroupsforuser"></a>戻り値 - getGroupsForUser

## <a name="method-getrolesforuser"></a>メソッド getRolesForUser

特定のユーザーのロールを取得します。

```xpp
public container getRolesForUser(str userName, str company)
```

### <a name="parameters---getrolesforuser"></a>パラメーター - getRolesForUser

userName  

<!-- -->

会社  

### <a name="return-value---getrolesforuser"></a>戻り値 - getRolesForUser

特定のユーザーのロールを保持するコンテナーです。

## <a name="method-getsidfromname"></a>メソッド getSIDFromName

特定のユーザー ログオン、ドメイン、および勘定タイプからのユーザーの詳細を取得します。

```xpp
public xAxaptaUserDetails getSIDFromName(str userLogin, str domainName, UserAccountType accountType)
```

### <a name="parameters---getsidfromname"></a>パラメーター - getSIDFromName

userLogin  

<!-- -->

domainName  

<!-- -->

accountType  

### <a name="return-value---getsidfromname"></a>戻り値 - getSIDFromName

ユーザーの詳細を含む xAxaptaUserDetails クラス インスタンス。

## <a name="method-getusersid"></a>メソッド getUserSid

```xpp
public str getUserSid(str username, str domain)
```

### <a name="parameters---getusersid"></a>パラメーター - getUserSid

username  

<!-- -->

domain  

### <a name="return-value---getusersid"></a>戻り値 - getUserSid

## <a name="method-validatedomain"></a>メソッド validateDomain

```xpp
public boolean validateDomain(str domain)
```

### <a name="parameters---validatedomain"></a>パラメーター - validateDomain

domain  

### <a name="return-value---validatedomain"></a>戻り値 - validateDomain

## <a name="method-validateorgunit"></a>メソッド validateOrgUnit

```xpp
public boolean validateOrgUnit(str ouName)
```

### <a name="parameters---validateorgunit"></a>パラメーター - validateOrgUnit

ouName  

### <a name="return-value---validateorgunit"></a>戻り値 - validateOrgUnit

## <a name="method-validatepassword"></a>メソッド validatePassword

```xpp
public boolean validatePassword(str username, str domain, str password)
```

### <a name="parameters---validatepassword"></a>パラメーター - validatePassword

username  

<!-- -->

domain  

<!-- -->

パスワード  

### <a name="return-value---validatepassword"></a>戻り値 - validatePassword

## <a name="method-validatesecgroup"></a>メソッド validateSecGroup

```xpp
public boolean validateSecGroup(str secGroup)
```

### <a name="parameters---validatesecgroup"></a>パラメーター - validateSecGroup

secGroup  

### <a name="return-value---validatesecgroup"></a>戻り値 - validateSecGroup

## <a name="method-new"></a>メソッド new

xAxaptaUserManager クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-updateuserroleassignments"></a>メソッド updateUserRoleAssignments

```xpp
public void updateUserRoleAssignments(UserId userId, container roles, container removeRoles)
```

### <a name="parameters---updateuserroleassignments"></a>パラメーター - updateUserRoleAssignments

userId  

<!-- -->

ロール  

<!-- -->

removeRoles  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

