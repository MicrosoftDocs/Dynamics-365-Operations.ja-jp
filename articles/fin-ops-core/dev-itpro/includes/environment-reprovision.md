---
ms.openlocfilehash: eb5ecef9cb9b70e8395989ea271bdb717e573427
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920495"
---
> [!IMPORTANT]
> 環境固有のレコードの中には、自動的なデータベース移動操作に含められないものがあり、その手順を追加する必要があります。 次のような役割があります。
> - Commerce セルフサービス インストーラー参照
> - Commerce Scale Unit チャネル データベースのコンフィギュレーション レコード

環境間でデータベースをコピーすると、次の追加の手順を実行しない限り、移行先環境の Commerce の機能は完全には機能しません。

### <a name="initialize-commerce-scale-units"></a>Commerce Scale Unit の初期化
データベースをサンドボックス UAT または実稼動環境に移動する場合は、データベースの移動操作が完了した後に、[Commerce Scale Unit を初期化](../deployment/Initialize-Retail-Channels.md)する必要があります。 ソース環境からの Commerce Scale Unit の関連付けは、移行先の環境にコピーされません。 

### <a name="synchronize-commerce-self-service-installers"></a>Commerce のセルフサービス インストーラーの同期
HQ 内の Commerce セルフサービス インストーラーにアクセスできるようにするには、データベースの移動操作が完了した後に[セルフサービス インストーラーを同期](../../../commerce/dev-itpro/synchronize-installers.md)する必要があります。

> [!IMPORTANT]
> 環境の再プロビジョニング手順は、データベース移動操作の一部として完全に自動化されており、これ以上手動で実行する必要はありません。 環境の再プロビジョニング ツールはアセット ライブラリで引き続き使用でき、特定の状況でエラーの状態を軽減するために使用される場合もあります。 

移行先の環境で環境の再プロビジョニング ツールを実行するには、次の手順を実行します。

1. **ソフトウェア配置可能パッケージ** セクションにある自身のプロジェクトの **アセット ライブラリ** で、 **インポート** を選択します。
2. 共用資産の一覧から、 **環境再プロビジョニング ツール** を選択します。
3. 移行先環境の **環境の詳細** ページで、 **管理** > **更新プログラムを適用** を順に選択します。
4. 先ほどアップロードした **環境再プロビジョニング** ツールを選択し、 **適用** を選択してパッケージを適用します。
5. パッケージの配置の進捗を監視します。

配置可能なパッケージの適用方法についての詳細は、 [配置可能なパッケージを作成する](../deployment/create-apply-deployable-package.md)を参照してください。 配置可能パッケージを手動で適用する方法の詳細については、 [配置可能 な パッケージ を コマンド ライン から インストール する](../deployment/install-deployable-package.md)を参照してください。

### <a name="re-activate-pos-devices"></a>POS デバイスの再アクティブ化

販売時点管理 (POS) デバイスを使用する場合は、データベースをインポートした後に、POS デバイスを再度アクティブ化する必要があります。 移行先環境で以前にアクティブ化されたデバイスは、機能しなくなります。 詳細については、[販売時点管理 (POS) デバイスのライセンス認証](../../../commerce/dev-itpro/retail-device-activation.md) を参照してください。