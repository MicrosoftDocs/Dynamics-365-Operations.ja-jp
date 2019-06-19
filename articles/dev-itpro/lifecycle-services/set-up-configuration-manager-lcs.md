---
title: 構成マネージャーの設定
description: このトピックでは、構成マネージャーの設定方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012, Operations
ms.custom: 62673
ms.assetid: 0845ab95-9597-4813-9967-e4f3815849ba
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 360511d7485046ae14748f22c2d4eeb026273b35
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595456"
---
# <a name="set-up-configuration-manager"></a>構成マネージャーの設定

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> この機能は、運用上の用途ではサポートされて**いません**。  構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。 これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。

## <a name="before-you-begin"></a>準備
開始する前に、環境には次のコンポーネントが含まれている必要があります。

- 業務に合わせてコンフィギュレーションされた実行中の AX 2012 R3 のバージョン。 AX 2012 R3 のインストール方法の詳細については、[Microsoft Dynamics AX 2012 のインストール](https://technet.microsoft.com/library/fbe52b68-1294-4398-b233-f8ec37c6d531(AX.60).aspx)を参照してください。
- 実行中のデータのインポート/エクスポート フレームワークのインスタンス。 データのインポート/エクスポート フレームワークをインストールする方法の詳細については、[データのインポート/エクスポート フレームワークをインストール (AX 2012)](./ax-2012/install-dixf.md) を参照してください。 

    > [!IMPORTANT]
    > データのインポート/エクスポート フレームワークへ接続するためには、構成マネージャー (ベータ) を有効にする DMFEntityExecutionStatusService および DMFService サービス グループを配置する必要があります。

- Lifecycle Services の AX 2012 R3 プロジェクトです。 

    > [!WARNING]
    > 環境間でコンフィギュレーションをコピーすることは破壊的な操作になります。 すべてのプロジェクト所有者は構成およびこれらの操作を実行する権限を持っています。 信頼されたユーザーのみがプロジェクト所有者として設定されていることを確認します。

## <a name="create-data-importexport-framework-source-data-formats-in-ax-2012-r3"></a>AX 2012 R3 でのデータのインポート/エクスポート フレームワーク ソース データ形式の作成
構成をエクスポートおよびインポートするすべての環境で構成を管理するには、Dynamics AX と CSV ソース データ形式の両方を作成する必要があります。

### <a name="create-an-ax-source-data-format"></a>AX ソース データ フォーマットを作成する

構成をエクスポートする環境で、次の手順を実行します。

1.  **データのインポート/エクスポート フレームワーク** &gt; **設定** &gt; **ソース データ形式**とクリックします。
2.  **新規**をクリックし、ソース AX の名前を付けます。
3.  タイプが **AX** であることを確認します。
4.  構成のインポート先の環境で、この手順を繰り返します。

### <a name="create-a-csv-source-data-format"></a>CSV ソース データ フォーマットを作成する

構成をエクスポートする環境で、次の手順を実行します。

1. **データのインポート/エクスポート フレームワーク** &gt; **設定** &gt; **ソース データ形式**とクリックします。
2. **新規**をクリックし、ソース CSV の名前を付けます。
3. タイプが **ファイル** であることを確認します。
4. **一般**タブで、次の値を設定します。

   |                  設定                  |     先頭値      |
   |-------------------------------------------|----------------|
   |       <strong>ファイル形式</strong>        |   区切り    |
   |     <strong>先頭行のヘッダー</strong>     |    選択済    |
   |      <strong>行区切り</strong>       |    {CR}{LF}    |
   |     <strong>列区切り</strong>     | 縦棒 { |
   |      <strong>テキスト修飾子</strong>      |       @@       |
   |         <strong>行をスキップ</strong>         |       0        |
   |        <strong>コード ページ</strong>         |      1252      |
   |     <strong>言語ロケール</strong>      |     EN-US      |
   | <strong>複数値の区切り</strong> |       ;        |

   ![構成マネージャーの DIXF 設定](./media/dixfconfigurationmanager.png)

5. 構成のインポート先の環境で、この手順を繰り返します。

## <a name="install-and-configure-the-local-component-of-the-system-diagnostics-lifecycle-services"></a>システム診断 (Lifecycle Services) のローカル コンポーネントのインストールと構成
構成をエクスポートする環境で、次の手順を実行します。 

> [!IMPORTANT]
> プロジェクトおよび環境のシステム診断のローカル コンポーネントを既にインストールしている場合、**プログラムの追加と削除**を使用し、アンインストールする必要があります。 検出されたインスタンスの数にかかわらず、環境ごとに 1 つの Microsoft Dynamics AX Application Object Server (AOS) だけが、コンフィギュレーションの管理と共に使用されます。

1.  システム診断のローカル コンポーネントをインストールします。 詳細については、[システム診断のインストールと実行 (Lifecycle Services)](./ax-2012/install-run-system-diagnostics-lcs.md) を参照してください。 重要: この beta リリースでは、システム診断のサービス アカウントを AX 2012 R3 の sysadmin ロールに追加する必要があります。
2.  **開始** &gt; **Microsoft Dynamics AX Lifecycle Services 診断サービス検索の順にクリックします**。
3.  **環境の検出**ウィンドウに、環境の名前と Microsoft SQL Server のインスタンスとデータベースの完全修飾名を入力します。 その後、[環境を検出] をクリックします。
4.  探索を完了した後、**コンフィギュレーション管理 (ベータ)** セクションに値を入力し、**保存**をクリックして、**アップロード環境**をクリックします。

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>オプション</th>
    <th>先頭値</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span class="ui">コンフィギュレーションの上書きを有効にする</span></td>
    <td>指定した AOS インスタンスのコンフィギュレーションをコピーし、上書きできるようにするには、このオプションを選択します。
    <p><strong>重要:</strong> 環境の設定が完了した際に、環境設定の上書きを無効にすることを強くお勧めします。</p>
    </td>
    </tr>
    <tr class="even">
    <td><span class="ui">AOS インスタンス</span></td>
    <td>コピーまたは上書きが可能な AOS インスタンスを指定します。</td>
    </tr>
    <tr class="odd">
    <td><span class="ui">保存場所</span></td>
    <td>構成のローカルの格納場所を指定します。 AOS サービス アカウントとデータのインポート/エクスポート フレームワーク サービス アカウントには、この場所への書き込みアクセス権が必要です。
    <p><strong>重要:</strong> データ インポート/エクスポート フレームワークに使用されているものと同じディレクトリを使用することを強く推奨します。インポートおよびエクスポートの内容によっては、共有ディレクトリに機密データが含まれていることがありますので注意してください。 出来る限りの少数のユーザーが、AOS サービス アカウントおよびデータのインポート / エクスポート フレームワーク サービス アカウントに加えて、その場所にアクセスできることを確認します。</p>
    </td>
    </tr>
    </tbody>
    </table>

    ![構成マネージャーのシステム診断の検出](./media/systemdiagnosticconfigurationmanagerdiscoverysettings.png)

5.  構成のインポート先の環境で、この手順を繰り返します。

## <a name="next-steps"></a>次のステップ
この環境は、設定をコピーして管理するための準備が整いました。 詳細については、[コンフィギュレーションのコピー (Lifecycle Services、LCS)](copy-configuration-lcs.md) を参照してください。



