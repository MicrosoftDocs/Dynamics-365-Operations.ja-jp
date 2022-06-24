---
title: クラウドおよびエッジ スケール ユニット用 Warehouse Management モバイル アプリの構成
description: この記事では、クラウドまたはエッジ スケール ユニットでサービスを提供している倉庫向けに、Warehouse Management のモバイル アプリを設定する方法について説明します。
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865241"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>クラウドおよびエッジ スケール ユニット用 Warehouse Management モバイル アプリの構成

[!include [banner](../includes/banner.md)]

この記事では、クラウドまたはエッジ スケール ユニットでサービスを提供している倉庫で使用するために、Warehouse Management のモバイルアプリを設定する方法について説明します。

## <a name="prerequisites"></a>必要条件

モバイル機器をクラウドやエッジ スケール ユニットに接続する設定を始める前に、エンタープライズ ハブに接続できるかどうかを確認します。 - 詳細については、[Warehouse Management モバイル アプリのインストールと接続](../warehousing/install-configure-warehouse-management-app.md) を参照してください。

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Warehouse Management モバイルアプリをスケール ユニットに対して実行した際の追加設定

[倉庫のスケールユニットのワークロードの展開プロセスの一環](cloud-edge-landing-page.md#scale-unit-manager-portal)として、Warehouse Management モバイル アプリのデバイスの接続に必要なデータのほとんどは、エンタープライズ ハブからスケールユニットに自動的に同期されます。 ただし、スケール ユニットのデプロイでは、**Azure Active Directory アプリケーション** ページ (**システム管理 \> 設定 \> Azure Active Directory アプリケーション**) でデータを入力する必要があります。 また、ユーザー ID の既定の **会社** 値を更新するか、新しいユーザーを作成する必要がある場合があります。 スケール ユニットの配置に存在しない会社に関連付けられているユーザーは、Warehouse Management モバイル アプリケーションをスケール ユニットに接続してもログインできません。

> [!NOTE]
> **Azure Active Directory アプリケーション** ページのデータは同期されていないため、倉庫のワークロードを別のスケール ユニットに移動させる場合は、手動でこのデータをメンテナンスする必要があります。

それぞれの Warehouse Management モバイル アプリの接続設定の一環として、指定された Azure Active Directory リソースの URL は、エンタープライズ ハブではなくスケール ユニットのものでなければならないことに注意してください。
