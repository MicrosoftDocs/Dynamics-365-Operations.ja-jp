---
title: 拡張機能にオーバーレイをリファクタリングするモデルの制限を緩和
description: このトピックでは、オーバーレイを拡張機能にリファクタリングできるように、モデルの制限を緩和する方法について説明します。 これは、モデルが Microsoft Dynamics 365 for Finance and Operations 8.0 にシールされているために、必要です。
author: CGarty
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: CGarty
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 3e4b1bc440d3bf62d8e932f9d45fe1f3bc56bfcb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409486"
---
# <a name="relax-model-restrictions-to-refactor-overlayering-into-extensions"></a>オーバーレイを拡張機能にリファクタリングするため、モデルの制限を緩和する

[!include [banner](../includes/banner.md)]

バージョン 8.0 以降の Finance and Operations アプリの開発ツールでは、オーバーレイヤリングを利用して Microsoft コードをカスタマイズすることができません。 動作の変更や追加には、拡張機能を使用する必要があります。 「オーバーレイを使用しない」という制限は、すべてのお客様が最新の機能と修正プログラムを利用できるように、アップデートが簡単で常に最新のバージョンで稼働するクラウドサービスをお客様に提供することに向けて、製品を進化させていく上で重要な部分です。

Dynamics AX 2012や Dynamics 365 for Finance and Operations バージョン7からコードをアップグレードした後で、オーバーレイを使用するカスタマイズを行った場合、コンパイル時にエラーが発生します。 コードのリファクタリングを行うには、オーバーレイされているモデルのモデル記述子ファイルで一時的にオーバーレイの制限を緩和できます。 この一時的な緩和は、開発環境およびデモ環境でのみ利用できます。スタンダード承認テスト以上のサンドボックス環境や実稼働環境などのランタイム環境には適用できません。 記述子の制限を緩和することで、段階的にコードを拡張機能へとリファクタリングし、コンパイル、実行、テストを行うことができます。 

## <a name="detailed-process"></a>詳細なプロセス
モデルの制限を緩和するには、以下の手順を実行します。 この手順は、クラウド環境で実行することも、ローカルの仮想マシン (VM) で実行することもできます。

1. Finance and Operations アプリの開発環境を展開します。 
2. Lifecycle Services (LCS) のコード アップグレード サービスを実行して、ソリューションをアップグレードします。
3. コンパイルできるように、必要に応じて Microsoft のモデルでのオーバーレイを一時的に許可します。
    
    a. C:\AOSService\PackagesLocalDirectory フォルダーで目的のモデルを見つけます。
    
    b. 記述子のフォルダーに移動します。 たとえば、\Currency\Descriptor フォルダーなどです。
    
    c. XML ファイルを開きます。 たとえば、Currency.xml ファイルなどです。
    
    d. **Customization** メタデータ要素を **AxModelInfo** メタデータ要素の内側に追加して、**AllowAndWarn** を指定します。ファイルの冒頭はこのようになります。
            
    ```xml
    <AxModelInfo xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
    <AppliedUpdates xmlns:d2p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" />
    <Customization>AllowAndWarn</Customization>
    ```
    
4. オーバーレイをリファクタリングして拡張機能にし、テストします。 ​オーバーレイを削除できるように、拡張機能を利用します。 必要な場合には、拡張機能の要求を行います。
5. Microsoft のモデルに対する一時的な変更を元に戻します。 オーバーレイを使用するモデルの展開はできなくなるため、記述子ファイルを更新することが重要です。
 
## <a name="prototyping-extensibility-requests"></a>拡張機能の要求のプロトタイピング
拡張機能を使用するようにソリューションを徐々に移行していく中で、ソリューションにおける課題を解消するために拡張機能の要求が必要になることがあります。 ソリューションの課題を解消し、拡張機能を使用するための移行プロセスをスムーズに進めるために何が必要なのかを十分に把握するために、拡張機能のプロトタイプを別のモデルとして作成することができます。

1. オーバーレイをリファクタリングするために必要な拡張機能を特定します。
2. 拡張機能のプロトタイプを拡張機能プロトタイプ モデルに追加します。

   - 列挙型の拡張については、対象の列挙型のコピーを拡張機能プロトタイプ モデルに追加して、拡張可能の設定を行います。
    
   - 抽出メソッドの拡張については、抽出されたメソッドとオーバーレイされたオリジナルのプロトタイプを拡張機能プロトタイプ モデルに作成します。
    
3. プロトタイプの拡張機能を使用します。
4. プロトタイプの拡張機能で問題がなければ、対応する要求を作成します。
5. その拡張機能をプラットフォームやアプリケーションに実装する際には、プロトタイプの拡張機能および関連するオーバーレイはすべて、拡張機能プロトタイプ モデルから削除する必要があります。
6. ソリューションのすべてのオーバーレイが拡張機能にリファクタリングされ、拡張機能プロトタイプ モデルが空になったら、ソリューションのリファクタリングは完了です。
