---
title: "仕入先ポータル ユーザー セキュリティ"
description: "この記事では、仕入先ポータルを使用する外部仕入先のセキュリティを設定する方法を説明します。 この情報は、2016 年 2 月 &amp; 2016 年 5 月バージョンの Dynamics AX にのみ適用されます。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8885f40a36eed1de7b0f6a2f369b1fc5a9d3fc8a
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-portal-user-security"></a>仕入先ポータル ユーザー セキュリティ

[!include[banner](../includes/banner.md)]


この記事では、仕入先ポータルを使用する外部仕入先のセキュリティを設定する方法を説明します。 この情報は、2016 年 2 月 &amp; 2016 年 5 月バージョンの Dynamics AX にのみ適用されます。

仕入先のポータルの機能は、Dynamics 365 for Operations バージョン 1611 で拡張された仕入先コラボレーション機能に変わりました。 仕入先コラボレーションのセキュリティ設定の詳細については、「[仕入先共同作業の設定と管理](set-up-maintain-vendor-collaboration.md)」を参照してください。 仕入先ポータルは、外部仕入先に発注書 (PO) に関する限定されたセットの情報を公開します。 お使いの Dynamics AX 環境の追加情報に仕入先が誤ってアクセスしないように、Microsoft Dynamics AX の仕入先ポータルのユーザーのアクセス許可を正しく設定することは重要です。 **重要:** 他のユーザーとは異なり、外部仕入先には**システム ユーザー**ロールがあるべきではありません。 **システム ユーザー**ロールは、外部ユーザーに適していない一連の機能へのアクセスを制御します。

## <a name="setting-up-a-vendor-portal-user"></a>仕入先ポータルのユーザー設定
仕入先ポータルを使用する誰かのユーザー アカウントを作成する前に、仕入先ポータルのコラボレーションを設定する仕入先を設定する必要があります。 **仕入先**ページの**概要**タブにある**発注書コラボレーション**フィールドを使用します。 仕入先ポータルを使用する外部仕入先は、次の設定をする必要があります。

-   仕入先の Microsoft Azure Active Directory (AAD) のユーザー アカウントを、Dynamics AX の**ユーザー**ページに登録する必要があります。
-   仕入先には、**システム ユーザー**ロールではなく、**仕入先 (外部)** セキュリティ ロールが必要です。 **注記:** Dynamics AX の新しいユーザー アカウントを作成するとき、**システム ユーザー**ロールが、自動的に付与されます。 したがって、そのロールを削除して、受信する警告メッセージを知らせる必要があります。
-   仕入先ユーザーに、発注書のビューに発注書のテーブルから追加のフィールドを追加するアクセス許可を付与すべきではありません。 **ユーザー**タブの、**個人用設定**タブで、**許可された明示的な個人用設定**オプションをユーザーに対し**いいえ**に設定します。
-   ユーザー アカウントは登録済の連絡担当者と関連付けられる必要があります。 **ユーザー**ページの、**名前**フィールドで連絡担当者を選択します。 選択した担当者には、関連する仕入先への**連絡先**ロールがあるべきです。

同じ担当者が複数の仕入先の仕入先ポータルへアクセスする必要がある場合 (おそらく、異なる法人に対して)、その人のユーザー アカウントのそれぞれが、同じ登録済の連絡担当者と関連付けられている必要があります。 **仕入先 (外部)** ロールには、仕入先ポータルで使用できる機能を使用するために必要な、すべての基本機能が含まれます。 この設定により、外部ユーザーに表示されるユーザー インターフェイスは対象とするシナリオのみにフォーカスするようにできます。

<a name="see-also"></a>参照
--------

[ベンダー コラボレーション](collaborate-vendors-vendor-portal.md)




