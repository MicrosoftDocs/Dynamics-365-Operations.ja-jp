---
title: 雇用検証 i9 検証
description: 連邦移民改革管理法 (IRCA) により、米国の雇用主は、新しく雇用した従業員の雇用適格性の状態を確認する必要があります。
author: ShielaSogge
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, HcmPersonIdentificationNumber, Hcmi9Document
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92480a8800571d477fcf00063e3303172274e595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752107"
---
# <a name="employment-verification-i9-verification"></a>雇用検証 i9 検証

[!include [banner](../../../includes/banner.md)]

連邦移民改革管理法 (IRCA) により、米国の雇用主は、新しく雇用した従業員の雇用適格性の状態を確認する必要があります。 この手順では、I-9 の検証に必要なドキュメントを記録する手順を説明します。 この手順では、USMF というデモ会社を使用します。

1. [人事管理] > [作業者] > [従業員] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、「Vince」という値を含む [名前] フィールドをフィルター処理します。
3. 従業員を選択します。 例: Vince Prado
4. [個人情報] クイック タブを展開します。
5. [ID 番号] をクリックします。
6. [新規] をクリックします。
7. 記録する ID タイプを選択します。 例: パスポート
8. [数] フィールドに値を入力します。
9. [基本] フィールドで、[はい] を選択します。
10. [説明] フィールドに、ID レコードの簡単な説明を入力します。
11. 発行機関で、作業者の ID のフォームを発行した機関を選択します。 例: 政府
12. 発行機関が作業者の ID のフォームを発行した日付を入力します。 例: 2011 年 2 月 15 日
13. ID のフォームの期限が切れる日付を入力します。 例: 2021 年 2 月 15 日
14. [保存] をクリックします。
15. ページを閉じます。
16. [雇用] タブをクリックします。
17. [I-9] をクリックします。
18. [新規] をクリックします。
19. [就業資格] フィールドで、オプションを選択します。
    * 従業員が米国の市民権または国籍を持っていない場合は、従業員の居住外国人番号または入国番号を入力する必要があります。  
20. [GroupListA] オプションを選択します。
    * 選択するリストは、従業員が提出した識別フォームにより決まります。 作業者は、リスト A のドキュメントを 1 つ、またはリスト B と C からドキュメントを 1 つ提出する必要があります。たとえば、作業者がパスポートを提示した場合、リスト A を選択することができます。 ただし、作業者が運転免許証と社会保障カードのみを提供した場合、リスト B と C を選択する必要があります。  
21. [ I-9 ドキュメント タイプ] フィールドで、従業員が提出したドキュメントのタイプを選択します。
22. [文章番号] フィールドで、値を入力または選択します。
23. [保存] をクリックします。



[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]