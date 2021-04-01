---
title: 仕入先ポータル ユーザー セキュリティ
description: この記事では、仕入先ポータルを使用する外部仕入先のセキュリティを設定する方法を説明します。 この情報は、2016 年 2 月 &amp; 2016 年 5 月バージョン Dynamics AX にのみ適用されます。
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68972e5ad773403001e5825dec57ff678a4e9b49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259845"
---
# <a name="vendor-portal-user-security"></a>仕入先ポータルのユーザー セキュリティ

[!include [banner](../includes/banner.md)]

この記事では、仕入先ポータルを使用する外部仕入先のセキュリティを設定する方法を説明します。 この情報は、2016 年 2 月 &amp; 2016 年 5 月バージョン Dynamics AX にのみ適用されます。

仕入先のポータルの機能は、Dynamics 365 for Operations バージョン 1611 で拡張された仕入先コラボレーション機能に変わりました。 仕入先コラボレーションのセキュリティ設定の詳細については、「[仕入先共同作業の設定と管理](set-up-maintain-vendor-collaboration.md)」を参照してください。 仕入先ポータルは、外部仕入先に発注書 (PO) に関する限定されたセットの情報を公開します。 お使いの Dynamics AX 環境の追加情報に仕入先が誤ってアクセスしないように、Microsoft Dynamics AX の仕入先ポータルのユーザーのアクセス許可を正しく設定することは重要です。 **重要:** 他のユーザーとは異なり、外部仕入先には **システム ユーザー** ロールがあるべきではありません。 **システム ユーザー** ロールは、外部ユーザーに適していない一連の機能へのアクセスを制御します。

## <a name="setting-up-a-vendor-portal-user"></a>仕入先ポータルのユーザー設定
仕入先ポータルを使用する誰かのユーザー アカウントを作成する前に、仕入先ポータルのコラボレーションを設定する仕入先を設定する必要があります。 **仕入先** ページの **概要** タブにある **発注書コラボレーション** フィールドを使用します。 仕入先ポータルを使用する外部仕入先は、次の設定をする必要があります。

-   仕入先の Azure Active Directory (AAD) のユーザー アカウントを、Dynamics AX の **ユーザー** ページに登録する必要があります。
-   仕入先には、**システム ユーザー** ロールではなく、**仕入先 (外部)** セキュリティ ロールが必要です。 **注記:** Dynamics AX の新しいユーザー アカウントを作成するとき、**SystemUser** ロールが、自動的に付与されます。 したがって、そのロールを削除して、受信する警告メッセージを知らせる必要があります。
-   仕入先ユーザーに、発注書のビューに発注書のテーブルから追加のフィールドを追加するアクセス許可を付与すべきではありません。 **ユーザー** タブの、**個人用設定** タブで、**許可された明示的な個人用設定** オプションをユーザーに対し **いいえ** に設定します。
-   ユーザー アカウントは登録済の連絡担当者と関連付けられる必要があります。 **ユーザー** ページの、**名前** フィールドで連絡担当者を選択します。 選択した担当者には、関連する仕入先への **連絡先** ロールがあるべきです。

同じ担当者が複数の仕入先の仕入先ポータルへアクセスする必要がある場合 (おそらく、異なる法人に対して)、その人のユーザー アカウントのそれぞれが、同じ登録済の連絡担当者と関連付けられている必要があります。 **仕入先 (外部)** ロールには、仕入先ポータルで使用できる機能を使用するために必要な、すべての基本機能が含まれます。 この設定により、外部ユーザーに表示されるユーザー インターフェイスは対象とするシナリオのみにフォーカスするようにできます。

<a name="additional-resources"></a>追加リソース
--------

[仕入先ポータルを使用して、仕入先と連携](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]