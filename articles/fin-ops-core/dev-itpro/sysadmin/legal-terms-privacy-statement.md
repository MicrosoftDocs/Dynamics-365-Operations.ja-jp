---
title: 組織の法律条項およびプライバシーに関する声明へのリンクの追加
description: このトピックでは、管理者がバージョン情報ウィンドウで、組織の法的条項およびプライバシーに関する声明へのリンクを追加する方法について説明します。
author: aneesmsft
ms.date: 10/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters, SysAbout
audience: IT Pro
ms.reviewer: sericks
ms.custom: 267894
ms.assetid: b74f8d8b-e20b-4ffd-8fd6-c64c2fe31c8a
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Application update 4
ms.openlocfilehash: 65e0fbbbca916230db11686e665b4beff9b3e4a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745975"
---
# <a name="add-links-to-your-organizations-legal-terms-and-privacy-statement"></a>組織の法律条項およびプライバシーに関する声明へのリンクの追加

[!include [banner](../includes/banner.md)]

このトピックでは、管理者が Microsoft Dynamics 365 Finance、Supply Chain Management、およびコマースの<strong>バージョン情報</strong>ウィンドウで、組織の法律条項およびプライバシーに関する声明にリンクを追加する方法について説明します。

組織は、多くの場合、法的およびコンプライアンス要件を満たすため、その法的な条件およびプライバシーに関する声明へのリンクをユーザーがすぐに入手して表示できるようにする必要があります。 組織の管理者は、以下の手順に従って、**バージョン情報** ウィンドウ (**設定** &gt; **バージョン情報**) で利用可能である法律条項とプライバシーに関する声明へのリンクを持つことができます。

## <a name="add-links"></a>リンクの追加
1.  **システム パラメーター** ページに移動し、**法的情報およびプライバシー** をクリックします。 このページでは:

    1.  組織の法的条件を説明するページへのリンクを入力します。

    2.  組織のプライバシーに関する声明を説明するページへのリンクを入力します。

        > [!NOTE]
        > *https* または *http* のいずれかで始まる完全な URL を入力していることを確認します。

2.  **保存** をクリックします。

3.  コマースを使用している場合は、**配送スケジュール** ページに移動します。 このページでは:

    1.  **1110 – グローバル構成** ジョブを選択します。

    2.  **今すぐ実行** をクリックします。

        > [!NOTE]
        > ジョブが完了したことを確認するには、**ダウンロード セッション** ページに移動します。

## <a name="validate-links"></a>リンクの検証

### <a name="validate-the-links-in-finance-supply-chain-management-and-commerce"></a>Finance、Supply Chain Management、およびコマースのリンクを検証

リンクが追加されたことを確認するには、ページ上部のツールバーで **設定** アイコンをクリックし、**詳細** をクリックします。 ウィンドウの **リンク** セクションに 2 つの新しいリンクが表示されます。

-   **お客様の組織の法律条項**
-   **お客様の組織のプライバシーと Cookie**

これらのリンクをクリックして、適切なページが開いていることを検証します。 

> [!NOTE]
> リンクが新しいウィンドウで開きますので、ポップアップ ブロッカーが有効になっている場合は、ポップアップ ブロック設定に例外を追加して新しいウィンドウを起動する必要があります。

### <a name="validate-the-links-in-modern-point-of-sale-mpos-and-cloud-point-of-sale-cpos"></a>Modern POS (MPOS) およびクラウド POS (CPOS) のリンクの検証
リンクが追加されたことを検証するには、**設定** ページにアクセスします。 **情報** セクションで、適切なページが開くことを検証するためにリンクをクリックします。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]