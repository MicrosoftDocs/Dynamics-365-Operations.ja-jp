---
title: セキュリティ ポリシーを作成する
description: この記事では、顧客グループの範囲に基づいて、顧客および顧客グループへのアクセスを保護する単純なセキュリティ ポリシーを作成する方法について説明します。
author: Peakerbl
ms.date: 07/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: sericks
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 21860124b0f02d5e6751943bdabcc8d22beb228b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898626"
---
# <a name="create-a-security-policy"></a>セキュリティ ポリシーを作成する
[!include [banner](../includes/banner.md)]

この記事では、顧客グループの範囲に基づいて、顧客および顧客グループへのアクセスを保護する単純なセキュリティ ポリシーを作成する方法について説明します。

## <a name="add-a-new-query"></a>新しいクエリの追加

1.  Visual Studio にて、プロジェクト/ソリューションに XDSQCustGroup10 などの新しいクエリを追加します。 クエリは、**制約** テーブルからのデータ アクセスを制限するために使用されます。

    ![新しいクエリを追加します。](media/71c5206330564e8c2612a61a5a211dba.png)

2.  **データ ソース** を右クリックし、**新しいデータ ソース** を選択します。

3.  **テーブル** フィールドで、プライマリ テーブル名を **CustGroup** と入力します。

4.  **範囲** を右クリックし、**新しい範囲** を選択します。

5.  **有効** フィールドを、**はい** に設定します。

6.  **データ ソース** フィールドで、プライマリ テーブル名を、この場合は「CustGroup」と入力します。

7.  **値フィールド** で **10** と入力して、CustGroup フィールドの範囲を定義することで、CustGroup の値が 10 であるデータへアクセスを制限します。

    ![値フィールドで、10 を入力します。](media/c970ccc0649fcd2ee4e2b9a9819eb2fc.png)

## <a name="add-a-new-security-policy"></a>新しいセキュリティ ポリシーの追加

1.  XDSCustTableOnCustGroup10 などの新しいセキュリティ ポリシーを追加します。

    ![セキュリティ ポリシーを追加します。](media/118355845fa679f8f004e516f0691cff.png)

2.  **制約付きテーブル** を **はい** に設定します。 これにより、プライマリ テーブルへのアクセスもセキュリティで保護されます。 この例では、これが **CustGroup** テーブルです。

3.  **コンテキスト タイプ** フィールドを **RoleName** に設定します。

4.  **有効** フィールドを、**はい** に設定します。

5.  **操作** フィールドを **AllOperations** に設定します。 **操作** の他の使用可能な値には、**選択**、**挿入**、**更新**、**削除**、および **InsertUpdateDelete** などがあります。

6.  **プライマリ テーブル** フィールドを **CustGroup** に設定します。

7.  **クエリ** フィールドに、上記で作成したクエリの名前、たとえば 「XDSQCustGroup10」 を設定します。

8.  **ロール名** フィールドを 「TradeSalesClerk」に設定します。 **コンテキスト タイプ** がこのポリシーの RoleName に設定されているため、ユーザー ロールの AOT 名を入力する必要があります。

    ![ロール名フィールドで、TradeSalesClerk を入力します。](media/9ad07f1e403cadfc3f1a52c2433e42c7.png)

8.  次に、制約されたテーブルを追加します。 この簡単な例では、テーブルを 1 つ追加します。

    ![制約付きテーブルを追加します。](media/e366725fa084d308b7f02a89a3e6175b.png)

    a.  **制約付きテーブル** を右クリックし、**新しい \> 制約付きテーブル** を選択します。

    b.  **制約付き** を **はい** に設定します。

    c.  **名前** フィールドで、制約付きテーブル、たとえば 「CustTable」 を入力します。

    d.  **テーブル リレーション** フィールドで、プライマリ テーブルにリレーション、この例では 「custgroup」 と入力します。

10.  最後の手順として、ソリューションをビルドおよび同期し、ポリシーを有効化する必要があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]