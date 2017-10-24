---
title: "電子申告コンフィギュレーション ライフサイクルの管理"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations ソリューションの電子申告 (ER) コンフィギュレーションのライフサイクルを管理する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 35288f5c2edfa8a340f963a5c7216041765a58b4
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>電子申告コンフィギュレーション ライフサイクルの管理

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Finance and Operations ソリューションの電子申告 (ER) コンフィギュレーションのライフサイクルを管理する方法について説明します。

<a name="overview"></a>概要
--------

電子申告 (ER) は、Microsoft Dynamics 365 for Finance and Operations の法律の要件および国固有の電子ドキュメントをサポートするエンジンです。 一般に、ER は、各電子ドキュメントに関して次のタスクの実行を想定しています。 詳細については、「[電子申告の概要](general-electronic-reporting.md)」を参照してください。

-   電子ドキュメントのテンプレートを設計します:
    -   ドキュメントに表示できるデータのソースを識別します:
        -   データ テーブル、データ エンティティ、クラスなど基になる Finance and Operations データ。
        -   実行日および時刻、タイム ゾーンなどプロセス固有のプロパティ。
        -   実行時にエンドユーザーが指定するユーザー入力パラメーター。
    -   必要なドキュメントの要素、および最終ドキュメントの形式を指定するトポロジを定義します。
    -   データソース経由でドキュメントの形式コンポーネントにバインドされ、定義されたドキュメント要素に選択したデータ ソースから要求されるデータ フローのコンフィギュレーションを行い、プロセスの制御ロジックを指定します。
-   他の Finance and Operations インスタンスでテンプレートが使用できるようにします:
    -   Finance and Operations で作成したドキュメント テンプレートを ER のコンフィギュレーションに変換し、現在の Finance and Operations インスタンスからコンフィギュレーションを XML パッケージとしてエクスポートし、ローカルまたは LCS に保存します。
    -   ER コンフィギュレーションを Finance and Operations ドキュメント テンプレートに変換します。
    -   ローカルまたは LCS に格納されている XML パッケージを、現在の Finance and Operations インスタンスにインポートします。
-   電子ドキュメント テンプレートをカスタマイズします:
    -   LCS からテンプレートを ER コンフィギュレーションとして現在の Finance and Operations インスタンスに取り込みます。
    -   基本バージョンを参照しながら、カスタム バージョンの ER コンフィギュレーションを設計します。
-   Finance and Operations で使用できるように、特定の業務プロセスを含むテンプレートを連結します:
    -   Finance and Operations の設定をコンフィギュレーションし、プロセスに関連したパラメーターでそのコンフィギュレーションを参照して、ER を使用開始できるようにします。 たとえば、特定の買掛金勘定の支払方法の ER コンフィギュレーションを参照して、請求書の処理についての電子支払メッセージを生成します。
-   特定の業務プロセスでテンプレートを使用します:
    -   特定の業務プロセスで ER コンフィギュレーションを実行します。 たとえば、ER コンフィギュレーションを参照する支払方法が選択された場合の請求書の処理についての電子支払メッセージの生成。

## <a name="concepts"></a>概念
次のロールおよび関連活動が、ER コンフィギュレーション ライフサイクルに関連付けられます。

| 役割                                       | 活動                                                      | 説明                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 電子申告機能コンサルタント | ER コンポーネントを作成および管理します (モデル、形式)。           | ER のドメイン固有のデータ モデルを設計し、電子ドキュメントの必須のテンプレートを作成し、それらを結合するビジネス ユーザー。                                                                           |
| 電子申告開発者             | データ モデルのマップを作成および管理します。                          | 必要な Finance and Operations データ ソースを選択し、ER のドメイン固有のデータ モデルに結合する Finance and Operations の専門家                                                                 |
| 会計監修者                      | ER のコンポーネントを参照するプロセス関連の設定を構成します。 | たとえば、特定の買掛金勘定支払方法で使用して請求書処理用に電子支払メッセージを生成する ER のコンフィギュレーション設定を許可する**会計監修者**のロール。 |
| 買掛金勘定支払係            | 特定の業務プロセスで ER コンポーネントを使用します。                | たとえば、特定の支払方法に対して構成されている ER 形式に基づいて請求書処理用に電子支払のメッセージが生成されるようにするのを許可する**買掛金勘定支払の担当者**ロール。           |

## <a name="er-configuration-development-lifecycle"></a>ER コンフィギュレーションの開発ライフサイクル
ER に関連する次の理由から、個別の Finance and Operations インスタンスとしての開発環境で、ER コンフィギュレーションを作成することをお勧めします:

-   **電子申告開発者**ロールまたは**電子申告機能コンサルタント**ロールのユーザーは、テスト目的でコンフィギュレーションを編集し、実行できます。 このシナリオでは、Finance and Operations インスタンスの業務データと業績について有害なおそれがあるクラスおよびテーブル メソッドが呼び出されることがあります。
-   ER コンフィギュレーションの ER データ ソースとしてのクラスおよびテーブル メソッドの使用は Finance and Operations エントリ ポイントおよび記録された会社の内容によって制限されません。 **電子申告開発者**ロールまたは**電子申告機能コンサルタント**ロールのユーザーは、機密情報にアクセスできます。

開発環境で設計された ER コンフィギュレーションは、コンフィギュレーション評価 (適切な統合プロセス、結果の正確性、パフォーマンス)、およびロールにおけるアクセス権の正確性、職務分掌など品質保証のために、テスト環境にアップロードできます。 ER コンフィギュレーションの交換を可能にする機能は、この目的に使用できます。 最後に、次の図に示すように、認定された ER コンフィギュレーションは、サービスのサブスクライバーと共有する LCS に、あるいは内部で使用する実稼働環境にアップロードできます。 ![ER コンフィギュレーション ライフサイクル](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>参照
--------

[電子申告の概要](general-electronic-reporting.md)




