---
title: "Talent 環境の削除"
description: "このトピックでは、Microsoft Dynamics 365 for Talent のテスト ドライブまたは実稼働環境の削除について説明します。"
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d1870c84d4d5e7402bae44d192ce7587c2f67fe7
ms.openlocfilehash: 0e7748b079b1cd5c069917d46e05cd281ea6aa01
ms.contentlocale: ja-jp
ms.lasthandoff: 04/05/2018

---
# <a name="remove-a-talent-environment"></a>Talent 環境の削除

このトピックでは、Microsoft Dynamics 365 for Talent のテスト ドライブまたは実稼働環境の削除について説明します。

## <a name="removing-a-test-drive-environment"></a>テスト ドライブ環境の削除

Talent テスト ドライブは、60 日間の有効期限ポリシーでプロビジョニングされます。 ただし、テスト ドライブ環境の所有者には、次の手順に従って早期にトライアルを終了するオプションがあります。 

1. [PowerApps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。
2. [環境] を選択します。
3. テスト ドライブ環境を選択します。これには、次のような命名パターンがあります。TestDrive - alias@domain
4. [削除] を選択し、決定内容を確認します。 

既存のテスト ドライブ環境が削除されます。 削除すると、新しいテスト ドライブ環境にサイン アップが可能です。 

## <a name="removing-a-production-environment"></a>実稼動環境の削除

このトピックでは、Talent をクラウド ソリューション プロバイダー、またはエンタープライズ アーキテクチャ (EA) 契約を通して購入したことを前提にしています。 

ひとつの Talent 環境がひとつの PowerApps 環境内に「含まれている」ため、考慮する 2 つのオプションがあります。 最初のオプションは、PowerApps 環境全体を削除することです。2 番目のオプションは、Talent のみを削除することです。 最初のオプションは、Talent をプロビジョニングする目的で特別に PowerApps 環境を作成し、実装を開始したばかりの場合、または既存の統合がない場合に優先されます。 2 つめのオプションは、PowerApps およびフローで活用されている豊富なデータが格納された PowerApps 環境が確立されている場合に適しています。

> [!Important]
> PowerApps 環境を削除する前に、それが Talent のスコープ外の豊富なデータ統合に使用されていないことを確認してください。 また、既定の PowerApps 環境を削除することはできないので注意してください。 

Talent や関連付けられたアプリ、およびフローを含む PowerApps 環境全体を削除するには。

1. [PowerApps 管理センター](https://admin.businessplatform.microsoft.com/) に移動します。
2. [環境] を選択します。
3. 削除する環境を選択してください。
4. [削除] を選択し、決定内容を確認します。 
5. 削除が完了するまで待ちます。
6. Talent をサブスクライブするために使用したアカウントを使用して [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) にサインインします。 
7. 環境を含む Talent プロジェクトを選択します。 
8. LCS プロジェクトでは、**Talent アプリの管理** タイルを選択します。 
9. 削除するインスタンスを選択します。 
10. [インスタンスの削除] を選択して決定内容を確認します。  

既存の PowerApps 環境から Talent 環境を削除するには、以下の手順を実行します。 Talent DevOps チームのサポートおよび連絡を含む必要性が、LCS で直接この機能が有効になるまでの一時的なものであることに注意してください。

1. サポートに連絡し、削除要求を開始してください。
2. サポート チームはTalent DevOps チームの削除リクエストを開始します。 
3. 環境が削除されたという知らせを受けた後に続行してください。
4.  Talent をサブスクライブするために使用したアカウントを使用して LCS にサインインします。 
5. 環境を含む Talent プロジェクトを選択します。 
6. LCS プロジェクトでは、**Talent アプリの管理** タイルを選択します。 
7. 削除するインスタンスを選択します。そのさい、配置ステータスが **失敗** とマークされている必要があります。
8. [インスタンスの削除] を選択して決定内容を確認します。 


