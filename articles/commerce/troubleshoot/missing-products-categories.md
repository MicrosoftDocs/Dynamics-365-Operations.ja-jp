---
title: 環境コピーの後に製品とカテゴリが欠落している
description: この記事では、環境間または同じ環境内でサイトがコピーされた後で製品とカテゴリが欠落している場合に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0c094f6da7756d2a6a3b80ebdb211d7b78148813
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851108"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>環境コピーの後に製品とカテゴリが欠落している

[!include [banner](../../includes/banner.md)]

この記事では、環境間または同じ環境内でサイトがコピーされた後で製品とカテゴリが欠落している場合に役立つトラブルシューティング ガイドを示します。

## <a name="description"></a>説明

サイトが環境間で、または同じ環境内でコピーされた後、製品とカテゴリはサイトから欠落します。 製品とカテゴリが e コマース サイト ビルダーで e コマース ウェブストアと **製品** タブから欠落しています。

## <a name="resolution"></a>解像度

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Commerce サイト ビルダーの新しくコピーされたサイトにチャンネルの作業単位番号をマップする

Commerce サイト ビルダーの新しくコピーされたサイトにチャンネルの作業単位番号 (OUN) をマップするには、次の手順を実行します。

1. 新しくコピーされたサイトを選択します。
1. **サイトの設定** で、**チャネル** を選択します。
1. チャネル名の横にある省略記号 (**...**) を選択し、**オンライン店舗チャネルの変更** を選択します 。
1. **オンライン店舗のチャネルの変更** ダイアログボックスで、新しくコピーされたサイトにマップするチャネルを選択し、**OK** を選択します。
1. **保存と公開** を選択します。

## <a name="additional-resources"></a>追加リソース

[オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け](../associate-site-online-store.md)
