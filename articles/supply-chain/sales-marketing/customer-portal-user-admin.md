---
title: 顧客ポータルのユーザーの作成と管理
description: このトピックでは、顧客ポータルのユーザー アカウントを作成し、アクセス権限の設定方法について説明します。
author: Henrikan
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 448f315b888b63eba74dcb8b47a9b238e371bb2b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573492"
---
# <a name="create-and-manage-customer-portal-users"></a>顧客ポータルのユーザーの作成と管理

[!include [banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

既定の実装では、ユーザーは顧客ポータルを使用して作成された Web サイトを自分で登録することはできません。 Web サイトにログインして使用するには、ユーザーが管理者で招待されている必要があります。マイクロソフトでは、ユーザーが登録を行う権限を意図的にブロックしています。

ユーザーが Web サイトを使用できるようにするには、そのユーザーに対して担当者レコードを作成しておく必要があります。 このレコードは、ユーザーが属する顧客アカウントとエンティティを示します。 この情報は、ユーザーが販売注文の作成と表示できることを保証するために不可欠です。

担当者レコードは、ユーザーが登録した際に自動的に作成されます。 そのため、ユーザーが正しい顧客アカウントとエンティティを選択しない可能性があります。 一方で、招待形式の処理では、招待の送信前に、管理者が正しい顧客アカウントとエンティティを担当者レコードに割り当てることができます。 ユーザーが自分で登録できるようなソリューションのカスタマイズを検討している場合は、想定される結果を必ず考慮してください。

## <a name="video"></a>ビデオ
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

[顧客を招待して、顧客ポータルへの登録と利用を促進する](https://youtu.be/drGUYHX9QIQ)  ビデオ (上記) は、YouTube で利用可能な [Finance and Operations のプレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)に含まれています。

## <a name="prerequisite-setup"></a>前提条件の設定

Power Apps ポータルの担当者は、Microsoft Dataverse の **担当者** テーブルにレコードとして保存されます。 デュアル書き込みでは、これらのレコードが必要に応じて Microsoft Dynamics 365 Supply Chain Management に同期されます。

![顧客ポータルの担当者で使用するシステム ダイアグラム。](media/customer-portal-contacts.png "顧客ポータルの担当者で使用するシステム ダイアグラム")

新たな顧客の招待をする前に、**担当者** テーブルのマッピングがデュアル書き込みで有効化されていることを確認してください。

## <a name="the-invitation-process"></a>招待の処理

顧客ポータルに既に存在する担当者を招待するには、Power Apps ポータル ドキュメントにおける [ポータルへの担当者への招待](/powerapps/maker/portals/configure/invite-contacts) に記載の手順に従ってください。

顧客を顧客ポータルに招待する前に、顧客の [担当者レコード ](/powerapps/maker/portals/configure/configure-contacts) が有効なものであり、次のように設定されていることを確認してください :

1. **会社** フィールドを、Supply Chain Management にて顧客を所属させる法人に設定します。
2. **顧客番号** フィールドを、Supply Chain Management にて顧客に設定する顧客アカウントの番号に設定します。

担当者の作成後は、Supply Chain Management でその担当者を表示できるようになります。

詳細については、Power Apps ポータル ドキュメントの [ポータルで使用する担当者の構成](/powerapps/maker/portals/configure/configure-contacts) を参照してください。

## <a name="out-of-box-web-roles-and-table-permissions"></a>既成の Web ロールとテーブルのアクセス許可

Power Apps ポータルのユーザー ロールは、[Web ロール](/powerapps/maker/portals/configure/create-web-roles) と [テーブルのアクセス許可](/powerapps/maker/portals/configure/assign-entity-permissions) によって定義されます。 既定では、顧客ポータルには少数のロールのみが定義されています。 新たなロールの作成、既存のロールの変更または削除が可能です。

### <a name="out-of-box-web-roles"></a>既成の Web ロール

このセクションでは、顧客ポータルと共に提供される既成の Web ロールについて説明します。

既成のユーザー ロールの変更方法の詳細については、Power Apps ポータル ドキュメントに記載の [ポータルで使用する Web ロールの作成](/powerapps/maker/portals/configure/create-web-roles) と [ポータルのテーブル権限を使用してレコードに基づくセキュリティを追加する](/powerapps/maker/portals/configure/assign-entity-permissions) を参照してください。

#### <a name="administrator"></a>管理者

管理者は、Web サイトの監視と管理をします。 このユーザーは、顧客ポータルの準備と設定を行います。 管理者は、ポータルを IT とセキュリティの観点から維持し、すべてが円滑に実行されるように管理します。 管理者は、新たな機能を追加したり、新たな役割を作成することによって、ポータルのカスタマイズや変更をすることもできます。

#### <a name="customer-representative"></a>顧客担当者

顧客の担当者は顧客の会社に勤務し、会社が発注する注文を管理します。 顧客の担当者は、会社が発注したすべての注文、およびそれら発注をしたユーザーを表示できます。 さらに、顧客担当者は、アカウント全体の情報を見ることができ、どの担当者がそのアカウントに代わって注文することができるかを確認できます。

#### <a name="authorized-users"></a>承認されたユーザー

承認されたユーザーは、発注処理や、発注した注文の状態を表示することができます。 社内の他のユーザーは、注文の状態を表示できません。

#### <a name="unauthorized-users"></a>承認されていないユーザー

承認されていないユーザーはデータを表示できません。 これらのユーザーは、契約条件などの公開された情報だけでなく、顧客ポータルを実行している会社に関する詳細情報を表示することもできます。

#### <a name="example"></a>例

次の表に、各 Web ロールのユーザーがシステム内で参照できる販売注文を示します。

| 販売注文 | 管理者 | 顧客 &nbsp;X の顧客代表者 | 承認されたユーザー : ジェーン | 承認されたユーザー : サム | 承認されていないユーザー : メイ |
|---|---|---|---|---|---|
| 顧客 &nbsp; X 発注者 : &nbsp; Jane | 有 | 有 | 有 | 無 | 無 |
| 顧客 &nbsp; X 発注者 : &nbsp; サム | 有 | 有 | 無 | 有 | 無 |
| 顧客 &nbsp; Y 発注者 : &nbsp; メイ | 有 | 無 | 無 | 無 | 無 |

> [!NOTE]
> サムとジェーンのどちらも顧客 X に勤務する担当者ですが、自分が発注した注文のみを表示でき、その他注文は表示されません。 メイは、システム内に注文があっても、承認されていないユーザーであるため、顧客ポータルで当該注文を表示することはできません。 (さらに、メイは顧客のポータル以外のチャネルを使用して発注している必要があります)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]