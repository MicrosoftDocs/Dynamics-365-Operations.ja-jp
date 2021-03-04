---
title: AX 2012 からのアップグレード - データ アップグレードのためのアップグレード前のチェックリスト
description: このトピックでは、Finance and Operations へのデータ アップグレードに関連付けられている、Microsoft Dynamics AX 2012 チェックリストの各タスクについて説明します。
author: jorisdg
manager: AnnBe
ms.date: 02/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 106163
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 456e574bf5d19d356057b40316b8b7b5b2e7ad41
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683967"
---
# <a name="upgrade-from-ax-2012---pre-upgrade-checklist-for-data-upgrade"></a>AX 2012 からのアップグレード - データ アップグレードのためのアップグレード前のチェックリスト

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

このトピックでは、Finance and Operations へのデータ アップグレードに関連付けられている、Microsoft Dynamics AX 2012 チェックリストの各タスクについて説明します。

## <a name="installation"></a>インストール
アップグレード前のチェックリストを使用して、アップグレード手順に必要なデータを入力します。 

- AX 2012 R3 からアップグレードする場合は、[KB 4035163](https://go.microsoft.com/fwlink/?linkid=852255) をインストールします
- AX 2012 R2 からアップグレードする場合は、[KB 4048614](https://go.microsoft.com/fwlink/?linkid=869025) をインストールします

## <a name="prepare-model-metadata"></a>モデル メタデータの準備

データ アップグレード中に、既存の AX 2012 環境と更新された Finance and Operations 環境との間で要素 ID を維持することが 1 つの目標です。 この目標を達成するには、AX 2012 環境の要素 ID のコピーを Finance and Operations 環境に移動する必要があります。 AX 2012 は、ModelElement という名前のテーブルに要素の ID を格納します。 このテーブルは、AX 2012 ビジネス データ データベースとは別のデータベースであるモデル データベースに含まれています。 Finance and Operations にアップグレード中に、Microsoft Azure に AX 2012 データベースをコピーする必要があります。 このプロセスには時間がかかる場合があります。 

model データベース全体を Azure SQL データベースにコピーしないようにするには、次の手順を使用して ModelElement テーブルをビジネス データ データベースに複製します。 後ほど、データのアップグレード実行中に、データベースの同期プロセスがこのレプリケートされたテーブルから必要な情報を取得し、アップグレードされた Finance and Operations 環境で要素 ID が管理されていることを確認します。

1. Finance and Operations データ アップグレードのチェックリストで、**セキュリティ モデル メタデータを準備する** をクリックします。
2. メッセージが表示されたら、**はい** をクリックします。
3. コピー処理が完了するまで待ちます。

プロセスが正常に行われた場合は、タスクは完了としてマークされています。

## <a name="prepare-security-role-metadata"></a>セキュリティ ロール メタデータの準備

データ アップグレード中のもう 1 つの目標は、セキュリティ ロールの割り当てを維持することです。 このタスクは、前の「モデル メタデータの準備」タスクに似ています。 AX 2012 モデル データベースに格納されているセキュリティ ロールの情報は、アップグレード後も情報が Finance and Operations 環境に残るように、AX 2012 ビジネス データ データベースにコピーする必要があります。 データ アップグレード中に、同じセキュリティ ロールはアップグレードされた Finance and Operations 環境に復元されます。

1. Finance and Operations データ アップグレードのチェックリストで、**セキュリティ ロール メタデータを準備する** をクリックします。
1. メッセージが表示されたら、**はい** をクリックします。
1. コピー処理が完了するまで待ちます。

プロセスが正常に行われた場合は、タスクは完了としてマークされています。

## <a name="set-up-user-mapping"></a>ユーザー マッピングの設定

AX 2012 では、ユーザーはオンプレミスの Active Directory サーバーで認証されます。 ただし、Finance and Operations では、ユーザーが Azure Active Directory (Azure AD) に対して認証されます。 このタスクは、既存の AX 2012 ユーザーを同等 Azure AD にマップするフォームを提供します。 AX 2012 ユーザーは、Finance and Operations にアクセスできるようになります。

1. Finance and Operations のデータ アップグレード チェックリストで、**ユーザー マッピングの設定** をクリックします。
2. **ユーザー情報電子メール マッピング** フォームが表示されます。 グリッドに記入するには、次のいずれかのステップを実行します。
   - AX 2012 からユーザーをインポートしてから、手動で Azure AD の電子メール アドレスを入力します。
       1. **AX からインポート** をクリックします。 グリッドには既存のユーザーが入力されます
       1. 各ユーザーについては、次の図に示すように、対応する Azure AD 電子メール アドレスを入力します。

           ![AX 2012 ユーザーの Azure AD 電子メール アドレス](media/userInfoEmailMapping.png)

   - ファイルからユーザーをインポートします。 このオプションは高速です。 多くのユーザーを更新する必要があるときは、このオプションを使用することをお勧めします。

     1. コンマ区切り値 (CSV) ファイルで、AX 2012 ユーザーと Azure AD 電子メール アドレスのマッピングを作成します。 IT 部門は、オンプレミスの Active Directory Domain Services (AD DS) から同様のマッピングをエクスポートできます。 このファイルには、**UserId** と **EmailAddress** の2つの列が含まれている必要があります。

         > [!NOTE]
         > ファイルの最初の行はヘッダー行として処理され、インポート時に無視されます。

     2. ファイルが準備できたら、**ファイルからのインポート** をクリックし、ファイルを参照してインポートします。

        グリッドには、ファイルで指定したマッピングを入力する必要があります。

インポートされたファイルには無効なエントリが含まれている場合は、エラー ファイルが生成されます。

## <a name="validate-baseline-version"></a>ベースライン バージョンの検証

現在のバージョンをアップグレードできることを検証するには、このタスクを実行します。

- Finance and Operations のデータ アップグレード チェックリストで、**ベースライン バージョンの検証** をクリックします。

ベースライン バージョンがサポートされているベースライン バージョンのいずれかの場合は、タスクは完了としてマークされます。


## <a name="archive-retail-salt-data"></a>小売 salt データのアーカイブ

このタスクは、RetailSaltUtility が使用するレジストリ キーを移行するために使用されます。 このツールは、チャンネル ユーザーの認証に使用されるハッシュに顧客が特定のランダム値を挿入する場所である、いくつかの配置に対して使用されます。

- Finance and Operations のデータ アップグレード チェックリストで、**小売 salt データのアーカイブ** をクリックします。

プロセスが正常に行われた場合は、タスクは完了としてマークされています。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]