---
title: 構成マネージャーを使用して構成をコピーする
description: 構成マネージャー (ベータ) 機能を使用すると、Microsoft Dynamics AX 2012 R3 の 1 つのインスタンスから他のインスタンスに構成をコピーすることができます。
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.custom: 15541
ms.assetid: 54283db7-6f1a-46e8-b74d-c67d54e6e5fb
ms.openlocfilehash: b050c6b1bec2f4311db204c6204848f3c8fc6f5a
ms.sourcegitcommit: 78d41eeef0a8a8e94ed502bd89778414231a31ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/17/2022
ms.locfileid: "9305140"
---
# <a name="copy-configurations-by-using-configuration-manager"></a>構成マネージャーを使用して構成をコピーする

[!include [banner](../includes/banner.md)]
[!include [LCS deprecation](../includes/lcs-deprecation.md)]

開始する前に、構成マネージャー (ベータ) を設定する必要があります。 詳細については、 [構成マネージャーの設定](set-up-configuration-manager-lcs.md) を参照してください。

> [!IMPORTANT]
> この機能は、運用上の用途ではサポートされて **いません**。 構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。 これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。


## <a name="export-a-configuration"></a>コンフィギュレーションのエクスポート
特定の法人およびエンティティからエクスポートすることにより、保存済みの構成を作成することができます。
1.  **エクスポートするコンフィギュレーション** リストで、プラス記号 (+) をクリックします。
2.  コンフィギュレーション名を入力し、**開始** をクリックします。
3.  保管場所を選択し、**続行** をクリックします。 ローカル、クラウド内、または両方の場所に、構成を保管することができます。
4.  接続先の環境を選択し、**続行** をクリックします。
5.  環境内のパーティションで使用できる法人を確認します。 処理する法人を選択し、**続行** をクリックします。
6.  保存されているコンフィギュレーションにコピーするエンティティを選択します。
7.  オプション: コンフィギュレーション データが含まれるがエンティティにはないテーブルは、保存されているコンフィギュレーションにコピーできません。 これらのテーブルを表示するには、**見つからないテーブル** タブをクリックします。
8.  保存された構成を作成するには、**続行** をクリックします。 コンフィギュレーションが作成された後、その内容を確認することができます。

## <a name="import-a-configuration"></a>コンフィギュレーションのインポート
1.  **インポートするコンフィギュレーション** リストで、既存のコンフィギュレーションを選択します。
2.  既定の名前を使用するか、新しい名前を入力します。 コンフィギュレーションは、ローカルおよびクラウドの両方に格納されている場合、保存されているコンフィギュレーションのインポート元を選択できます。 **続行** をクリックします。
3.  コンフィギュレーションをインポートする環境を選択し、**続行** をクリックします。
4.  環境内のパーティションで使用できる会社を確認します。 インポート元の会社の場所 (たとえば、initialDAT) を選択することによってと連携する会社を選択し、**続行** をクリックします。
5.  保存されているコンフィギュレーションにコピーするエンティティを選択します。
6.  保存された構成をインポートするには、**続行** をクリックします。 コンフィギュレーションが作成された後、その内容を確認することができます。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
