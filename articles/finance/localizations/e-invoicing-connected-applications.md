---
title: 接続されているアプリケーション
description: この記事では、電子請求で接続されているアプリケーションを設定する方法について説明します。
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f908caa902e4747d324480e3a5108b443d385ea7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277334"
---
# <a name="connected-applications"></a>接続されているアプリケーション

[!include [banner](../includes/banner.md)]

接続されたアプリケーションは、Regulatory Configuration Service (RCS) から利用できる Microsoft Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management のインスタンスです。 接続されたアプリケーションを通じて、Finance および Supply Chain Management のグローバリゼーション機能の一部を構成することで、電子請求書のシナリオを実現することができます。

グローバリゼーション機能を展開する場合、Finance or Supply Chain Management アプリケーションに適用される設定情報を、RCS から適切に接続されたアプリケーションに直接公開できます。

RCS の Finance または Supply Chain Management パラメーターを使用できると、ユーザー受入れテスト (UAT) や運用環境など複数のアプリケーション環境があり、同じパラメーターを異なる環境に展開して設定の一貫性を保つのが簡単になります。

## <a name="create-a-connected-application"></a>接続されたアプリケーションを作成する

1. RCS アカウントにサインインします。
2. **グローバリゼーション機能** ワークスペースの **環境t** セクションで、**電子請求** タイルを選択します。
3. **環境の設定** ページのアクション ウィンドウで、**接続されたアプリケーション** を選択します。
4. **新規** を選択して、接続されたアプリケーションを作成します。
5. **名前** フィールドに、接続するアプリケーションの名前を入力します。
6. **タイプ** フィールドで、**Dynamics 365 Finance** を選択します。
7. **アプリケーション** フィールドに、接続する環境の URL を入力します。
8. **テナント** フィールドに、環境のテナントを入力します。
9. **保存** を選択します。
10. アクション ウィンドウで、**接続の確認** を 選択して環境との接続をテストします。 テスト後、ページを閉じます。

## <a name="link-connected-applications-to-environments"></a>接続されたアプリケーションと環境の関連付け

1. **環境の設定** ページで **新規** を選択し、接続されたアプリケーションを環境に割り当てます。
2. **接続されたアプリケーション**  フィールドで、接続されたアプリケーションを選択します。
3. **サービス環境** フィールドで、サービスの環境を選択します。
4. **保存** を選択し、ページを閉じます。
