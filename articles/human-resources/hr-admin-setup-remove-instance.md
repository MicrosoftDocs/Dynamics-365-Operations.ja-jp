---
title: インスタンスの削除
description: この記事では、Microsoft Dynamics 365 Human Resources のテスト ドライブ環境または実稼動環境の削除について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a40b9619e92b81272208ad4241a2455330a342a7
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124431"
---
# <a name="remove-an-instance"></a>インスタンスの削除

この記事では、Microsoft Dynamics 365 Human Resources のテスト ドライブ環境または実稼動環境の削除について説明します。

## <a name="remove-a-test-drive-environment"></a>テスト ドライブ環境の削除

人事管理のテスト ドライブは、60 日間の有効期限ポリシーでプロビジョニングされます。 ただし、テスト ドライブ環境の所有者には、次の手順に従って早期にトライアルを終了するオプションがあります。 

1. [Power Apps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。
2. **環境**を選択します。
3. テスト ドライブ環境を選択します。これには、次のような命名パターンがあります: TestDrive - alias@domain
4. **削除**を選択し、決定内容を確認します。 

既存のテスト ドライブ環境が削除されます。 削除すると、新しいテスト ドライブ環境にサイン アップが可能です。 

## <a name="remove-a-production-environment"></a>実稼動環境の削除

この記事では、人事管理をクラウド ソリューション プロバイダー (CSP) またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。 

ひとつの人事管理環境がひとつの Power Apps 環境内に含まれているため、2 つのオプションを考慮できます。 最初のオプションは、Power Apps 環境全体を削除することです。2 番目のオプションは、人事管理のみを削除することです。 最初のオプションは、人事管理をプロビジョニングする目的で特別に Power Apps 環境を作成し、実装を開始したばかりの場合、または既存の統合がない場合に優先されます。 2 つめのオプションは、Power Apps および Power Automate で活用されている豊富なデータが格納された Power Apps 環境が確立されている場合に適しています。

> [!Important]
> Power Apps 環境を削除する前に、それが人事管理のスコープ外の豊富なデータ統合に使用されていないことを確認してください。 また、既定の Power Apps 環境を削除することはできないので注意してください。 

人事管理や関連付けられたアプリ、およびフローを含む Power Apps 環境全体を削除するには:

1. [Power Apps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。
2. **環境**を選択します。
3. 削除する環境を選択してください。
4. **削除**を選択し、決定内容を確認します。 
5. 削除が完了するまで待ちます。
6. 人事管理をサブスクライブするために使用したアカウントを使用して [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) にサインインします。 
7. 環境を含む人事管理プロジェクトを選択します。 
8. LCS プロジェクトでは、**人事管理アプリの管理**タイルを選択します。 
9. 削除するインスタンスを選択します。 
10. **インスタンスの削除**を選択して決定内容を確認します。  

既存の Power Apps 環境から人事管理環境を削除するには、以下の手順を実行します。 人事管理 DevOps チームのサポートおよび連絡を含む必要性が、LCS で直接この機能が有効になるまでの一時的なものであることに注意してください。

1. サポートに連絡し、削除要求を開始してください。
2. サポート チームは、人事管理チームの削除リクエストを開始します。 
3. 環境が削除されたという知らせを受けた後に続行してください。
4.  人事管理をサブスクライブするために使用したアカウントを使用して LCS にサイン インします。 
5. 環境を含む人事管理プロジェクトを選択します。 
6. LCS プロジェクトでは、**人事管理アプリの管理**タイルを選択します。 
7. 削除するインスタンスを選択します。そのさい、配置ステータスが **失敗** とマークされている必要があります。
8. **インスタンスの削除**を選択して決定内容を確認します。 
