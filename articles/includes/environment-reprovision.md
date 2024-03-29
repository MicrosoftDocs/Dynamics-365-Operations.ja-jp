---
ms.openlocfilehash: 22911afd3a3da0ce3bcaeb7e42ab0096c868be547d559f14a91e09d6e6e12c08
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777067"
---
環境間でデータベースをコピーするとき、コピーされたデータベースが完全に機能するには、その前に環境の再プロビジョニング ツールを実行して、すべての Commerce コンポーネントを確実に最新にしておく必要があります。

> [!IMPORTANT]
> Commerce 機能はすべての環境に含まれているため、Commerce コンポーネントを使用しているかどうかに関係なく、この手順を実行することをお勧めします。 

続行する前に、次の前提条件が満たされていることを確認する必要があります。
1. 2017 年 7 月リリース (7.2 とも呼ばれる) 7.2.11792.56024 にアップグレードする場合は、移行先環境にアプリケーション X++ 修正プログラムを適用してから、その環境内でデータのアップグレードを実行します。 これにより、データ アップグレード中の各種エラーの発生を防止します。

    - KB 4036156 - Retail マイナー バージョン アップグレード - 'バリアント番号順序が設定されていません。' この修正プログラム パッケージには、KB 4035399 および KB 4035751 も含まれています。 このパッケージを使用するには、最低でも Platform Update 9 が必要であることに注意してください。 確信が持てない場合は、最新のバイナリをインストールしてください。
    
2. Microsoft Dynamics AX 2012 からアップグレードする場合は、データ アップグレードを実行する前に、移行先の環境に次のアプリケーション X++ 修正プログラムをインストールします。
    - KB 4033183 - Dynamics AX 2012 R2 または Dynamics AX 2012 R3 Pre-CU8 non-retail アップグレードは、dbo.RETAILTILLLAYOUTZONE のオブジェクトが存在しないため失敗しました。
    - KB 4040692 - Microsoft Dynamics 365 for Operations 7.2 への Dynamics AX 2012 R3 のアップグレードは、SalesLineIdx に RetailSalesLine の重複インデックスが存在するため失敗しました。
    - KB 4035490 - GeneralJournalAccountEntry MainAccount フィールドのアップグレード スクリプトに関するパフォーマンスの問題。


以下のステップに従って、環境再プロビジョニング ツールを実行します。

1. 共有アセット ライブラリで、**ソフトウェア配置可能パッケージ** を選択します。
2. 環境再プロビジョニング ツールをダウンロードします。
3. 自身のプロジェクトのアセット ライブラリで、**ソフトウェア配置可能パッケージ** を選択します。
4. **新規作成** を選択して、新しいパッケージを作成します。
5. パッケージの名前と説明を入力します。 **環境再プロビジョニング ツール** をパッケージ名として使用できます。
6. 先ほどダウンロードしたパッケージをアップロードします。
7. ターゲット環境の **環境の詳細** ページで、 **管理** > **更新プログラムを適用** を順に選択します。
8. 先ほどアップロードした環境再プロビジョニング ツールを選択し、**適用** を選択してパッケージを適用します。
9. パッケージの配置の進捗を監視します。 

配置可能パッケージを適用する方法の詳細については、 [配置可能パッケージの適用](../deployment/create-apply-deployable-package.md)を参照してください。 配置可能パッケージを手動で適用する方法の詳細については、 [配置可能パッケージのインストール](../deployment/install-deployable-package.md)を参照してください。
