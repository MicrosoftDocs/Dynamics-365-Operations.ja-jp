---
title: Microsoft Dynamics 365 Talent - Attract の電子メール設定のコンフィギュレーション
description: このトピックでは、Microsoft Dynamcis 365 Talent - Attract で送信される電子メールのコンフィギュレーション方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c891a36f01d36774bd921475fa5995d207cd2d51
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008665"
---
# <a name="configure-email-settings"></a>電子メール設定のコンフィギュレーション

[!include[banner](../includes/banner.md)]

ブランドは信頼を確立し、候補者がポジションに応募する前に、候補者との関係を構築するのに役立ちます。 ポジティブなブランド認識は、優秀な人材を引き付け、既に在籍している従業員のロイヤルティを高めます。 Microsoft Dynamics 365 Talent: Attract を使用すると、会社のブランドを反映するように電子メールを構成できます。 したがって、職務候補者が応募プロセスを進めていくにつれて、候補者に一貫したエクスペリエンスを提供することができます。

Attract を使用すると、次のアクションを実行できます。

- 会社の Microsoft Exchange 電子メール サービス アカウントが使用されるように電子メールの設定をコンフィギュレーションします。 このようにして、候補者は電子メールがあなたの会社から送られているということを認知します。 たとえば、候補者が `contoso@microsoft.com` の代わりに、`recruiting@contoso.com` から電子メールを受け取るように設定することができます。
- 電子メール テンプレートにグローバル ヘッダーおよびフッターを設定することで、すべての電子メール通信に一貫したブランドを作成します。 

> [!NOTE]
> 会社の電子メール サービス アカウントを使用して電子メールを送信できるようにするためには、包括採用アドオンが必要です。

## <a name="connect-an-email-service-account"></a>電子メール サービス アカウントの接続

会社の電子メールサービス アカウントを接続することにより、求職者に対してブランド化された電子メール エクスペリエンスを作成することができます。 会社のアカウントに接続していない場合、Attract は既定の Microsoft ブランドの電子メール サービス アカウントを使用します。

1. **設定** (右上隅にあるギヤ記号) を選択してから、**管理センター**を選択します。
2. **電子メール設定**タブの**電子メール サービス アカウント**で、**会社のアカウントへの接続**を選択します。

    ![会社の電子メール サービス アカウントを Attract に接続する](./media/attract-admin-email-service-accounts.png)

    共有メール アカウントの作成方法については、[Exchange Online の共有メールボックス](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes)を参照してください。

3. Microsoft のサインイン ウィンドウで、会社の資格情報を使用してサインインします。
4. まだ電子メール サービス アカウントを設定していない場合、または新しいアカウントを追加する場合は**新しいサービス アカウントの追加**を選択し、電子メール情報を入力します。 使用する電子メール サービス アカウントを既に設定している場合は、それを選択します。

電子メール サービス アカウントのコンフィギュレーションが正常に完了すると、**電子メール サービス アカウント**の下に一覧表示されます。

## <a name="disconnect-an-email-service-account"></a>電子メール サービス アカウントの接続解除

Attract を使用した電子メール通信で会社のドメインの使用を中止したい場合は、電子メール サービス アカウントを接続解除できます。

1. **設定** (右上隅にあるギヤ記号) を選択してから、**管理センター**を選択します。
2. **電子メール設定**タブの**電子メール サービス アカウント**で、接続を解除する電子メール サービス アカウントの横にある**詳細**ボタン (縦の 3 つの点) を選択します。
3. **電子メール アカウントの接続解除**を選択します。

    ![会社の電子メール サービス アカウントを接続解除する](./media/attract-admin-disconnect-email-account.png)

4. 操作を確認するメッセージが表示されたら、**接続解除**を選択します。

    ![会社の電子メール サービス アカウントの接続解除を確認する](./media/attract-admin-email-confirm-disconnect.png)

別の電子メール サービス アカウントに接続しない場合、Attract から送信された電子メールには、既定の Microsoft ブランドの電子メール サービス アカウントが使用されます。

## <a name="configure-email-template-settings"></a>電子メール テンプレート設定のコンフィギュレーション

会社のロゴの画像やその他の情報を、ブランド化されたヘッダーとして電子メールにアップロードすることができます。 また、プライバシー ポリシーおよび使用条件へのリンクを、電子メール フッターで提供することもできます。

> [!NOTE]
> お客様は、ご自身の所在国や地域における法律、および電子メールの受信者の所在国や地域における法律を遵守する必要があります。 これらの法律には、スパム規制が含まれます。

1. **設定** (右上隅にあるギヤ記号) を選択してから、**管理センター**を選択します。
2. **メール設定**タブの**電子メール テンプレート設定**で、メール ヘッダーとして使用する画像をイメージ ボックスにドラッグするか、イメージ ボックスをクリックしてファイルを参照します。 既存の画像を置き換えるには、まずその横にある**削除**を選択する必要があります。 画像は、JPEG、JPG、PNG、または SVG ファイルにする必要があります。 推奨される画像のサイズは、幅 25 ~ 800 ピクセルで、高さが 25 ~ 150 ピクセルです。 ヘッダーの最大ファイル サイズは 1 メガ バイト (MB) です。

    ![会社の電子メール ヘッダーの画像の追加](./media/attract-admin-email-header.png)

3. **通信に関するプライバシー ポリシー**には、会社のプライバシー ポリシーへのリンクを記載してください。 **通信に関する使用条件**には、会社の使用条件へのリンクを記載してください。

    ![会社のプライバシー ポリシーおよび電子メール フッターの使用条件へのリンクを追加する](./media/attract-admin-email-footer.png)

4. **保存**を選択して、電子メール テンプレート設定を保存します。
