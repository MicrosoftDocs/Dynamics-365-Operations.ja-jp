---
title: 高度な倉庫管理へのアップグレードおよび移行のトラブルシューティング
description: このトピックでは、高度な倉庫管理へのアップグレードおよび移行中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993889"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>高度な倉庫管理へのアップグレードおよび移行のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、高度な倉庫管理へのアップグレードおよび移行中に発生する可能性がある問題を修正する方法について説明します。

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>エラー メッセージ "java.security.cert.certPathValidatorException: 証明書パスのトラスト アンカーが見つかりません" が表示されます。

### <a name="issue-description"></a>問題の説明

オンプレミス環境の Android 8 以上で自己署名証明書が信頼されていない場合に、このエラー メッセージが倉庫アプリに表示されます。

### <a name="issue-resolution"></a>問題の解決

外部 (パブリック) 証明機関 (CA) を使用します。 この問題の修正プログラムは、ウェアハウス アプリのバージョン 1.9.0.0 で入手できます。 この問題と修正方法の詳細については、[ウェアハウス アプリの接続の問題のトラブルシューティング](troubleshoot-warehouse-app-connection.md)を参照してください。

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>基本倉庫管理から高度な倉庫管理に移行するために承認されたプロセスは何ですか。

### <a name="issue-description"></a>問題の説明

現在、在庫管理を実行していて基本在庫機能を使用しており、モバイル デバイス、ウェーブ、および作業を活用するために、高度な在庫管理に移行しようとしています。 ただし、この移行を試みると問題が発生します。 たとえば、保管分析コード (サイト、倉庫、および場所) を使用するように製品を変更することはできません。製品にはそれらに対するトランザクションが含まれているためです。 そのため、基本倉庫管理から高度な倉庫管理に移行するために承認されたプロセスについて学習する必要があります。

### <a name="issue-resolution"></a>問題の解決

基本倉庫管理から高度な倉庫管理に移行するプロセスの詳細については、次のブログの投稿とドキュメントを参照してください。

- [既存の品目と倉庫で倉庫管理プロセスを有効にする](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Microsoft Dynamics AX WMS と新しい R3 倉庫および輸送機能への移行](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [WMSI/WMS2 項目の移行](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [倉庫管理を Microsoft Dynamics AX 2012 から Supply Chain Management にアップグレードする](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
