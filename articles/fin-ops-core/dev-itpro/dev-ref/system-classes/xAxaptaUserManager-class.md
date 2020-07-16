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
# <a name="class-xaxaptausermanager"></a><span data-ttu-id="feabb-103">クラス xAxaptaUserManager</span><span class="sxs-lookup"><span data-stu-id="feabb-103">Class xAxaptaUserManager</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xAxaptaUserManager extends Object
```

## <a name="remarks"></a><span data-ttu-id="feabb-104">備考</span><span class="sxs-lookup"><span data-stu-id="feabb-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="feabb-105">例</span><span class="sxs-lookup"><span data-stu-id="feabb-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="feabb-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="feabb-106">Methods</span></span>

| <span data-ttu-id="feabb-107">方法</span><span class="sxs-lookup"><span data-stu-id="feabb-107">Method</span></span>                                                                                               | <span data-ttu-id="feabb-108">説明</span><span class="sxs-lookup"><span data-stu-id="feabb-108">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="feabb-109">public container enumerateDomains(str server)</span><span class="sxs-lookup"><span data-stu-id="feabb-109">public container enumerateDomains(str server)</span></span>                                                        |                                                                        |
| <span data-ttu-id="feabb-110">public xAxaptaUserDetails enumerateDomainUsers(str domainName)</span><span class="sxs-lookup"><span data-stu-id="feabb-110">public xAxaptaUserDetails enumerateDomainUsers(str domainName)</span></span>                                       |                                                                        |
| <span data-ttu-id="feabb-111">public str generatePassword()</span><span class="sxs-lookup"><span data-stu-id="feabb-111">public str generatePassword()</span></span>                                                                        |                                                                        |
| <span data-ttu-id="feabb-112">public xAxaptaUserDetails getDomainUser(str domainName, str userLogin)</span><span class="sxs-lookup"><span data-stu-id="feabb-112">public xAxaptaUserDetails getDomainUser(str domainName, str userLogin)</span></span>                               |                                                                        |
| <span data-ttu-id="feabb-113">public str getFQDN(str domainName, \[boolean throwError\])</span><span class="sxs-lookup"><span data-stu-id="feabb-113">public str getFQDN(str domainName, \[boolean throwError\])</span></span>                                           |                                                                        |
| <span data-ttu-id="feabb-114">public container getGroupsForUser(str userName)</span><span class="sxs-lookup"><span data-stu-id="feabb-114">public container getGroupsForUser(str userName)</span></span>                                                      |                                                                        |
| <span data-ttu-id="feabb-115">public container getRolesForUser(str userName, str company)</span><span class="sxs-lookup"><span data-stu-id="feabb-115">public container getRolesForUser(str userName, str company)</span></span>                                          | <span data-ttu-id="feabb-116">特定のユーザーのロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="feabb-116">Gets roles for the given user.</span></span>                                         |
| <span data-ttu-id="feabb-117">public xAxaptaUserDetails getSIDFromName(str userLogin, str domainName, UserAccountType accountType)</span><span class="sxs-lookup"><span data-stu-id="feabb-117">public xAxaptaUserDetails getSIDFromName(str userLogin, str domainName, UserAccountType accountType)</span></span> | <span data-ttu-id="feabb-118">特定のユーザー ログオン、ドメイン、および勘定タイプからのユーザーの詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="feabb-118">Gets user details from the given user logon, domain, and account type.</span></span> |
| <span data-ttu-id="feabb-119">public str getUserSid(str username, str domain)</span><span class="sxs-lookup"><span data-stu-id="feabb-119">public str getUserSid(str username, str domain)</span></span>                                                      |                                                                        |
| <span data-ttu-id="feabb-120">public boolean validateDomain(str domain)</span><span class="sxs-lookup"><span data-stu-id="feabb-120">public boolean validateDomain(str domain)</span></span>                                                            |                                                                        |
| <span data-ttu-id="feabb-121">public boolean validateOrgUnit(str ouName)</span><span class="sxs-lookup"><span data-stu-id="feabb-121">public boolean validateOrgUnit(str ouName)</span></span>                                                           |                                                                        |
| <span data-ttu-id="feabb-122">public boolean validatePassword(str username, str domain, str password)</span><span class="sxs-lookup"><span data-stu-id="feabb-122">public boolean validatePassword(str username, str domain, str password)</span></span>                              |                                                                        |
| <span data-ttu-id="feabb-123">public boolean validateSecGroup(str secGroup)</span><span class="sxs-lookup"><span data-stu-id="feabb-123">public boolean validateSecGroup(str secGroup)</span></span>                                                        |                                                                        |
| <span data-ttu-id="feabb-124">public void new()</span><span class="sxs-lookup"><span data-stu-id="feabb-124">public void new()</span></span>                                                                                    | <span data-ttu-id="feabb-125">xAxaptaUserManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="feabb-125">Initializes a new instance of the xAxaptaUserManager class.</span></span>            |
| <span data-ttu-id="feabb-126">public void updateUserRoleAssignments(UserId userId, container roles, container removeRoles)</span><span class="sxs-lookup"><span data-stu-id="feabb-126">public void updateUserRoleAssignments(UserId userId, container roles, container removeRoles)</span></span>         |                                                                        |
| <span data-ttu-id="feabb-127">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="feabb-127">public void finalize()</span></span>                                                                               |                                                                        |

## <a name="method-enumeratedomains"></a><span data-ttu-id="feabb-128">メソッド enumerateDomains</span><span class="sxs-lookup"><span data-stu-id="feabb-128">Method enumerateDomains</span></span>

```xpp
public container enumerateDomains(str server)
```

### <a name="parameters---enumeratedomains"></a><span data-ttu-id="feabb-129">パラメーター - enumerateDomains</span><span class="sxs-lookup"><span data-stu-id="feabb-129">Parameters - enumerateDomains</span></span>

<span data-ttu-id="feabb-130">server</span><span class="sxs-lookup"><span data-stu-id="feabb-130">server</span></span>  

### <a name="return-value---enumeratedomains"></a><span data-ttu-id="feabb-131">戻り値 - enumerateDomains</span><span class="sxs-lookup"><span data-stu-id="feabb-131">Return Value - enumerateDomains</span></span>

## <a name="method-enumeratedomainusers"></a><span data-ttu-id="feabb-132">メソッド enumerateDomainUsers</span><span class="sxs-lookup"><span data-stu-id="feabb-132">Method enumerateDomainUsers</span></span>

```xpp
public xAxaptaUserDetails enumerateDomainUsers(str domainName)
```

### <a name="parameters---enumeratedomainusers"></a><span data-ttu-id="feabb-133">パラメーター - enumerateDomainUsers</span><span class="sxs-lookup"><span data-stu-id="feabb-133">Parameters - enumerateDomainUsers</span></span>

<span data-ttu-id="feabb-134">domainName</span><span class="sxs-lookup"><span data-stu-id="feabb-134">domainName</span></span>  

### <a name="return-value---enumeratedomainusers"></a><span data-ttu-id="feabb-135">戻り値 - enumerateDomainUsers</span><span class="sxs-lookup"><span data-stu-id="feabb-135">Return Value - enumerateDomainUsers</span></span>

## <a name="method-generatepassword"></a><span data-ttu-id="feabb-136">メソッド generatePassword</span><span class="sxs-lookup"><span data-stu-id="feabb-136">Method generatePassword</span></span>

```xpp
public str generatePassword()
```

### <a name="return-value---generatepassword"></a><span data-ttu-id="feabb-137">戻り値 - generatePassword</span><span class="sxs-lookup"><span data-stu-id="feabb-137">Return Value - generatePassword</span></span>

## <a name="method-getdomainuser"></a><span data-ttu-id="feabb-138">メソッド getDomainUser</span><span class="sxs-lookup"><span data-stu-id="feabb-138">Method getDomainUser</span></span>

```xpp
public xAxaptaUserDetails getDomainUser(str domainName, str userLogin)
```

### <a name="parameters---getdomainuser"></a><span data-ttu-id="feabb-139">パラメーター - getDomainUser</span><span class="sxs-lookup"><span data-stu-id="feabb-139">Parameters - getDomainUser</span></span>

<span data-ttu-id="feabb-140">domainName</span><span class="sxs-lookup"><span data-stu-id="feabb-140">domainName</span></span>  

<!-- -->

<span data-ttu-id="feabb-141">userLogin</span><span class="sxs-lookup"><span data-stu-id="feabb-141">userLogin</span></span>  

### <a name="return-value---getdomainuser"></a><span data-ttu-id="feabb-142">戻り値 - getDomainUser</span><span class="sxs-lookup"><span data-stu-id="feabb-142">Return Value - getDomainUser</span></span>

## <a name="method-getfqdn"></a><span data-ttu-id="feabb-143">メソッド getFQDN</span><span class="sxs-lookup"><span data-stu-id="feabb-143">Method getFQDN</span></span>

```xpp
public str getFQDN(str domainName, [boolean throwError])
```

### <a name="parameters---getfqdn"></a><span data-ttu-id="feabb-144">パラメーター - getFQDN</span><span class="sxs-lookup"><span data-stu-id="feabb-144">Parameters - getFQDN</span></span>

<span data-ttu-id="feabb-145">domainName</span><span class="sxs-lookup"><span data-stu-id="feabb-145">domainName</span></span>  

<!-- -->

<span data-ttu-id="feabb-146">throwError</span><span class="sxs-lookup"><span data-stu-id="feabb-146">throwError</span></span>  

### <a name="return-value---getfqdn"></a><span data-ttu-id="feabb-147">戻り値 - getFQDN</span><span class="sxs-lookup"><span data-stu-id="feabb-147">Return Value - getFQDN</span></span>

## <a name="method-getgroupsforuser"></a><span data-ttu-id="feabb-148">メソッド getGroupsForUser</span><span class="sxs-lookup"><span data-stu-id="feabb-148">Method getGroupsForUser</span></span>

```xpp
public container getGroupsForUser(str userName)
```

### <a name="parameters---getgroupsforuser"></a><span data-ttu-id="feabb-149">パラメーター - getGroupsForUser</span><span class="sxs-lookup"><span data-stu-id="feabb-149">Parameters - getGroupsForUser</span></span>

<span data-ttu-id="feabb-150">userName</span><span class="sxs-lookup"><span data-stu-id="feabb-150">userName</span></span>  

### <a name="return-value---getgroupsforuser"></a><span data-ttu-id="feabb-151">戻り値 - getGroupsForUser</span><span class="sxs-lookup"><span data-stu-id="feabb-151">Return Value - getGroupsForUser</span></span>

## <a name="method-getrolesforuser"></a><span data-ttu-id="feabb-152">メソッド getRolesForUser</span><span class="sxs-lookup"><span data-stu-id="feabb-152">Method getRolesForUser</span></span>

<span data-ttu-id="feabb-153">特定のユーザーのロールを取得します。</span><span class="sxs-lookup"><span data-stu-id="feabb-153">Gets roles for the given user.</span></span>

```xpp
public container getRolesForUser(str userName, str company)
```

### <a name="parameters---getrolesforuser"></a><span data-ttu-id="feabb-154">パラメーター - getRolesForUser</span><span class="sxs-lookup"><span data-stu-id="feabb-154">Parameters - getRolesForUser</span></span>

<span data-ttu-id="feabb-155">userName</span><span class="sxs-lookup"><span data-stu-id="feabb-155">userName</span></span>  

<!-- -->

<span data-ttu-id="feabb-156">会社</span><span class="sxs-lookup"><span data-stu-id="feabb-156">company</span></span>  

### <a name="return-value---getrolesforuser"></a><span data-ttu-id="feabb-157">戻り値 - getRolesForUser</span><span class="sxs-lookup"><span data-stu-id="feabb-157">Return Value - getRolesForUser</span></span>

<span data-ttu-id="feabb-158">特定のユーザーのロールを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="feabb-158">A container that holds roles for the given user.</span></span>

## <a name="method-getsidfromname"></a><span data-ttu-id="feabb-159">メソッド getSIDFromName</span><span class="sxs-lookup"><span data-stu-id="feabb-159">Method getSIDFromName</span></span>

<span data-ttu-id="feabb-160">特定のユーザー ログオン、ドメイン、および勘定タイプからのユーザーの詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="feabb-160">Gets user details from the given user logon, domain, and account type.</span></span>

```xpp
public xAxaptaUserDetails getSIDFromName(str userLogin, str domainName, UserAccountType accountType)
```

### <a name="parameters---getsidfromname"></a><span data-ttu-id="feabb-161">パラメーター - getSIDFromName</span><span class="sxs-lookup"><span data-stu-id="feabb-161">Parameters - getSIDFromName</span></span>

<span data-ttu-id="feabb-162">userLogin</span><span class="sxs-lookup"><span data-stu-id="feabb-162">userLogin</span></span>  

<!-- -->

<span data-ttu-id="feabb-163">domainName</span><span class="sxs-lookup"><span data-stu-id="feabb-163">domainName</span></span>  

<!-- -->

<span data-ttu-id="feabb-164">accountType</span><span class="sxs-lookup"><span data-stu-id="feabb-164">accountType</span></span>  

### <a name="return-value---getsidfromname"></a><span data-ttu-id="feabb-165">戻り値 - getSIDFromName</span><span class="sxs-lookup"><span data-stu-id="feabb-165">Return Value - getSIDFromName</span></span>

<span data-ttu-id="feabb-166">ユーザーの詳細を含む xAxaptaUserDetails クラス インスタンス。</span><span class="sxs-lookup"><span data-stu-id="feabb-166">A xAxaptaUserDetails class instance that contains user details.</span></span>

## <a name="method-getusersid"></a><span data-ttu-id="feabb-167">メソッド getUserSid</span><span class="sxs-lookup"><span data-stu-id="feabb-167">Method getUserSid</span></span>

```xpp
public str getUserSid(str username, str domain)
```

### <a name="parameters---getusersid"></a><span data-ttu-id="feabb-168">パラメーター - getUserSid</span><span class="sxs-lookup"><span data-stu-id="feabb-168">Parameters - getUserSid</span></span>

<span data-ttu-id="feabb-169">username</span><span class="sxs-lookup"><span data-stu-id="feabb-169">username</span></span>  

<!-- -->

<span data-ttu-id="feabb-170">domain</span><span class="sxs-lookup"><span data-stu-id="feabb-170">domain</span></span>  

### <a name="return-value---getusersid"></a><span data-ttu-id="feabb-171">戻り値 - getUserSid</span><span class="sxs-lookup"><span data-stu-id="feabb-171">Return Value - getUserSid</span></span>

## <a name="method-validatedomain"></a><span data-ttu-id="feabb-172">メソッド validateDomain</span><span class="sxs-lookup"><span data-stu-id="feabb-172">Method validateDomain</span></span>

```xpp
public boolean validateDomain(str domain)
```

### <a name="parameters---validatedomain"></a><span data-ttu-id="feabb-173">パラメーター - validateDomain</span><span class="sxs-lookup"><span data-stu-id="feabb-173">Parameters - validateDomain</span></span>

<span data-ttu-id="feabb-174">domain</span><span class="sxs-lookup"><span data-stu-id="feabb-174">domain</span></span>  

### <a name="return-value---validatedomain"></a><span data-ttu-id="feabb-175">戻り値 - validateDomain</span><span class="sxs-lookup"><span data-stu-id="feabb-175">Return Value - validateDomain</span></span>

## <a name="method-validateorgunit"></a><span data-ttu-id="feabb-176">メソッド validateOrgUnit</span><span class="sxs-lookup"><span data-stu-id="feabb-176">Method validateOrgUnit</span></span>

```xpp
public boolean validateOrgUnit(str ouName)
```

### <a name="parameters---validateorgunit"></a><span data-ttu-id="feabb-177">パラメーター - validateOrgUnit</span><span class="sxs-lookup"><span data-stu-id="feabb-177">Parameters - validateOrgUnit</span></span>

<span data-ttu-id="feabb-178">ouName</span><span class="sxs-lookup"><span data-stu-id="feabb-178">ouName</span></span>  

### <a name="return-value---validateorgunit"></a><span data-ttu-id="feabb-179">戻り値 - validateOrgUnit</span><span class="sxs-lookup"><span data-stu-id="feabb-179">Return Value - validateOrgUnit</span></span>

## <a name="method-validatepassword"></a><span data-ttu-id="feabb-180">メソッド validatePassword</span><span class="sxs-lookup"><span data-stu-id="feabb-180">Method validatePassword</span></span>

```xpp
public boolean validatePassword(str username, str domain, str password)
```

### <a name="parameters---validatepassword"></a><span data-ttu-id="feabb-181">パラメーター - validatePassword</span><span class="sxs-lookup"><span data-stu-id="feabb-181">Parameters - validatePassword</span></span>

<span data-ttu-id="feabb-182">username</span><span class="sxs-lookup"><span data-stu-id="feabb-182">username</span></span>  

<!-- -->

<span data-ttu-id="feabb-183">domain</span><span class="sxs-lookup"><span data-stu-id="feabb-183">domain</span></span>  

<!-- -->

<span data-ttu-id="feabb-184">パスワード</span><span class="sxs-lookup"><span data-stu-id="feabb-184">password</span></span>  

### <a name="return-value---validatepassword"></a><span data-ttu-id="feabb-185">戻り値 - validatePassword</span><span class="sxs-lookup"><span data-stu-id="feabb-185">Return Value - validatePassword</span></span>

## <a name="method-validatesecgroup"></a><span data-ttu-id="feabb-186">メソッド validateSecGroup</span><span class="sxs-lookup"><span data-stu-id="feabb-186">Method validateSecGroup</span></span>

```xpp
public boolean validateSecGroup(str secGroup)
```

### <a name="parameters---validatesecgroup"></a><span data-ttu-id="feabb-187">パラメーター - validateSecGroup</span><span class="sxs-lookup"><span data-stu-id="feabb-187">Parameters - validateSecGroup</span></span>

<span data-ttu-id="feabb-188">secGroup</span><span class="sxs-lookup"><span data-stu-id="feabb-188">secGroup</span></span>  

### <a name="return-value---validatesecgroup"></a><span data-ttu-id="feabb-189">戻り値 - validateSecGroup</span><span class="sxs-lookup"><span data-stu-id="feabb-189">Return Value - validateSecGroup</span></span>

## <a name="method-new"></a><span data-ttu-id="feabb-190">メソッド new</span><span class="sxs-lookup"><span data-stu-id="feabb-190">Method new</span></span>

<span data-ttu-id="feabb-191">xAxaptaUserManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="feabb-191">Initializes a new instance of the xAxaptaUserManager class.</span></span>

```xpp
public void new()
```

## <a name="method-updateuserroleassignments"></a><span data-ttu-id="feabb-192">メソッド updateUserRoleAssignments</span><span class="sxs-lookup"><span data-stu-id="feabb-192">Method updateUserRoleAssignments</span></span>

```xpp
public void updateUserRoleAssignments(UserId userId, container roles, container removeRoles)
```

### <a name="parameters---updateuserroleassignments"></a><span data-ttu-id="feabb-193">パラメーター - updateUserRoleAssignments</span><span class="sxs-lookup"><span data-stu-id="feabb-193">Parameters - updateUserRoleAssignments</span></span>

<span data-ttu-id="feabb-194">userId</span><span class="sxs-lookup"><span data-stu-id="feabb-194">userId</span></span>  

<!-- -->

<span data-ttu-id="feabb-195">ロール</span><span class="sxs-lookup"><span data-stu-id="feabb-195">roles</span></span>  

<!-- -->

<span data-ttu-id="feabb-196">removeRoles</span><span class="sxs-lookup"><span data-stu-id="feabb-196">removeRoles</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="feabb-197">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="feabb-197">Method finalize</span></span>

```xpp
public void finalize()
```

