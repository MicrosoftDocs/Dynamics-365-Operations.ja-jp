---
title: Finance and Operations バージョン 10.0 (2019 年 4 月) の新機能および変更された機能
description: このトピックでは Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 のプレビュー中の機能について説明します。 このバージョンは、2019 年 4 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: a362a31d-44df-45c5-b698-64c5264c592e
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: Release 10
ms.openlocfilehash: 36de8a786f8dd13d9c56fa5737433cc15291b039
ms.sourcegitcommit: 529763612e8af315d588e85ba807a5c849df57bf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/25/2019
ms.locfileid: "894691"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-100-april-2019"></a>Finance and Operations バージョン 10.0 (2019 年 4 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 10.0.8 です。 バージョン 10.0 の詳細については [追加リソース](whats-new-changed-10.md#additional-resources) を参照してください。

Microsoft Dynamics 365 for Retail の機能については [Dynamics 365 for Retail (2019 年 4 月) の新機能および変更された機能](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/april-whats-new) を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化

Finance and Operations の今回のリリースでは、列挙、メタデータ、メソッドの強化など、拡張性をサポートするために、さまざまな拡張機能の強化が加えられています。 詳細については、[Dynamics 365 for Finance and Operations バージョン 10.0 で変更された拡張機能](../../dev-itpro/extensibility/extensibility-changes-10.md)を参照してください。

## <a name="catch-weight-product-processing-with-warehouse-management"></a>倉庫管理による CW 製品の処理
この機能を使用すると、倉庫管理プロセス内の CW 製品を使用できます。 この機能は、今回のリリースの制限対象者のみに提供できます。 

詳細については、[倉庫管理の CW 製品処理](../../supply-chain/warehousing/catch-weight-processing.md) を参照してください。

## <a name="master-planning-stability-and-recovery-improvements"></a>マスター プランの安定性と復元性の改善

マスター プランが、継続的な改善を行うことにより不具合や接続の問題に対してより柔軟な対応ができるようになります。 これにより、マスタープランの機能が強化され、例外処理により中断されることなく復旧できます。

以前はマスター プランが停止した場合は、マスター プランの再実行する必要がありました。 このプロセスが改善され、マスター プランが中断した場合は自動的に停止した地点から再開するようになりました。 これはマスタープランにおいて時間を重視するお客様にとって重要な改善点となります。

##  <a name="improved-removal-of-obsolete-planning-data"></a>使われていないプランデータの削除機能を改善しています

マスター プランが正常に実行された後、不要になったプランデータをクリーンアップ ジョブが削除するよう設定されています。 マスター プランの実行時に不備があった際には、データのクリーンアップはされません。そのため不要なデータの収集をしてしまうリスクを回避できます。

クリーンアップ ジョブは機能強化されており、以前に失敗したマスタープランの実行データを削除します、また他の処理スレッドをブロックすることなく、使用可能なすべてのヘルパーが実行されるようを最適化されています。 これらの機能強化は、会社間マスタ プランにも適用されています。

## <a name="realize-the-conditional-tax-when-postdated-checks-are-drawn"></a>先日付小切手が引き落とされたときに条件付税を現金化する

条件付加税とは、一部の国/地域で必要とされる現金対象の付加価値税 (VAT) です。 請求書の支払を行うまでは、この税を差し引くことができます。 支払方法が先日付小切手の場合は、支払いの際、または先日付小切手が引き落とされる際に税金を現金化するオプションがあります。 このオプションを有効にするには **現金および銀行管理パラメーター > 先日付小切手 > 先日付小切手が引き落とされるときに、条件付け税を現金化** に移動します。 詳細については、「 [条件付消費税](../../financials/general-ledger/indirect-taxes-overview.md#conditional-sales-tax) 」を参照してください。 

## <a name="non-gst-transactions-for-india"></a>インド向けの非販売税トランザクション 
この機能を使用すると、税エンジンを使用して非販売税トランザクションを作成できます。 非販売税トランザクションを作成するには、それぞれの課税対象トランザクション行の **税情報** で **非販売税** チェック ボックスを選択します。 また、**参照番号順序グループ** に **供給の請求** の **番号順序コード** があることも確認する必要があります。 これらのトランザクションは、販売税還付 (GSTR) で非販売税トランザクションとして識別されます。 

## <a name="tax-engine"></a>税エンジン

> [!NOTE]
> 税エンジン (GTE) は、現在のみインドのみで使用可能となっています。

今回のリリースには、税エンジンを対象とする次の機能が含まれています。

### <a name="improving-tax-configuration-usability-with-reduced-number-of-lookups"></a>参照処理を削減することで、税コンフィギュレーションの操作性が向上しました

税エンジン (GTE) を使用して税をコンフィギュレーションする際に、税率、非控除割合、税コンポーネント、税期間を参照する複数のテーブルを定義することができます。 この機能を使って組み合わせの設定をすることで、参照する テーブルの数を削減することができます。 たとえば、 **原産国/地域** 、 **消費国/地域** 、および **製品タイプ** などの データ モデル プロパティは、いろいろな場所で流用することができる税トランザクションの種類を決定します。 今回のリリースでは、参照が可能な明細行レベルで文字列型の判定を追加することができます。 この測定は、レポートやレートなど、他の参照でさらに使用できます。

この機能により、管理が必要な参照処理の件数を大幅に削減することができ、税コンフィギュレーションの操作性が向上します。 この明細行レベルの文字列型の判定機能は、税ドキュメントのユーザー インターフェイスにも表示されます。

### <a name="simplifying-tax-setup-maintenance-with-excel-integration"></a>Excelとの機能統合により、税設定のメンテナンスが簡素化されます

税コンフィギュレーションにて、税金の設定パラメーター(税率を設定および非控除割合 など) を管理することは、一部の国/地域や業種によってはこの作業に手間がかかってしまいます。 今回は Microsoft Excel のファイルでこれらの管理を行うことができるようになっています。このファイルは税参照テーブルに基づいて自動生成され、税設定と機能統合されています。

### <a name="enabling-tax-configuration-with-tax-currency-and-sales-tax-codes"></a>税通貨および消費税コードによる税コンフィギュレーションの有効化

GTE における消費税コードはの設定は、Finance and Operationsと機能統合するうえで必須となります。 これまでは、 GTE が税コンフィギュレーションを同期する際に税コンポーネントと同名の消費税コードを生成しており、この消費税コードの自動生成には通貨会計が使用されています。

世界中の複数の税を登録する必要のある会社は、異なる国で使用されている税通貨を税コンポーネントで管理する必要があります。 今回のリリースでは、次の機能をご利用いただけます。

- 税設定にて消費税コードを管理します。
- 参照テーブルの消費税コードに税コンポーネントを割り当てます。
- これらの消費税コードの税通貨と決済期間を管理します。

税の設定にあたり、 GTE は税取引を記録するために、割り当てられた消費税コード、税の通貨および決済期間を使用します。

## <a name="expanded-regional-coverage-for-regulatory-configuration-service-rcs-deployments"></a>Regulatory Configuration Service (RCS)が展開される対象地域の拡充
RCSへの機能拡張を継続的に行っていく一環として、対象地域を拡大しており、ここではエンドユーザーがサービス環境を任意に配置することが可能です。 今回のリリースの一部として、ユーザーは次の国または地域でRCS環境をホストすることができます。

- 米国 
- インド 
- ヨーロッパ (プレビュー)
- 中国 (プレビュー)

## <a name="tax-functionality-updates-for-china"></a>中国に向けた税機能のアップデート

中国では、正式なタックスインボイスは政府が承認した2つのインボイスソフトウェア (AisinoとBaiWang) のみが発行することができます。 この機能では発行されたインボイスを、.TXTおよび. XMLファイル形式にエクスポートし、それらファイルを必要に応じて承認されたソフトである Aisino と BaiWang にインポートすることができます。 

Finance and Operations の税分類とコードを管理することも可能です。これは税統合インターフェイス3.0と整合性を保ちます。 請求書をエクスポートしたファイルには、中国では必須となっている商品コード (商品やサービスの分類) が含まれています。 

標準カテゴリ階層の設定には、エクスポートしたファイル内にインボイスの明細行に商品コードを含める機能が実装されています。

このリリースでは次の更新が含まれています。

- BaiWangが提供するソフトとの間に新たなインターフェイスが実装されており、BaiWangのソフトウェアから出力された .TXT形式と.XML形式のファイルをインポートでき、発行されたインボイスを .XML形式で出力することができます。
- 発行するインボイスの構成が更新されたため、Aisinoが提供するソフトウェアに .TXT ファイルをインポートして連携することが可能となりました。

詳細については、 [中国の税統合の構成](../../financials/localizations/apac-chn-tax-integration.md) を参照してください。

## <a name="electronic-reporting-er"></a>電子申告 (ER)

今回のリリースには、電子申告 (ER)に関する次の機能が含まれています。

### <a name="performance-optimization-of-customer-built-configurations"></a>ユーザーが行ったコンフィギュレーションに対するパフォーマンスの最適化
機能コンサルタントである「ペルソナ」が、電子申告 コンフィギュレーションの実行を記録することができます。 このコンサルタントは生成された記録を分析し、使用頻度の高いノードをキャッシュすることで電子申告 コンフィギュレーションパフォーマンスの最適化します。

これまでは、キャッシュの対象となっていたものは一定のレコードのみであり、処理に関連するレコードはキャッシュされていませんでした。 この機能は、入れ子構造のレコードをキャッシュすることができます。 また、本機能を使うことで 「ずる賢い」キャッシュを行うことができます。 参照されたレコードのみをキャッシュし、全体をキャッシュしません。

### <a name="setting-up-parameters-by-legal-entity"></a>法人別パラメーターの設定

この機能では、抽象データソースを含むER形式の構成をすることができ、法人ユーザーがどのようにデータ ソースを入力するか指定することができます。 ビジネス ユーザーは、Finance and Operationsのインターフェースを使って指定した法人のマスターデータをもとにERフォーマットを設定することができます。 これは、対応するERフォーマットの実行を制御する可能性のある法人に対して行うことができます。

この機能では、 ビジネス ユーザー が Finance and Operations インスタンスから特定の企業のERフォーマットをマスターデータとともにエクスポートし、もう一方へとインポートすることができます。

### <a name="specify-a-custom-storage-location-for-generated-documents"></a>生成されたドキュメント用にカスタマイズされた保存先を指定します

新たなERの拡張点としては、コードを作成することができ、その中でERフォーマットが生成されるドキュメントにアクセスすることが可能なイベントに参加できます。 ERフレームワークに対応したファイルの保存先を拡張することができ、ドキュメントを継続的に保存していくことが可能です。

詳細については、次の [生成されたドキュメントの保管場所を指定する](../../dev-itpro/analytics/er-custom-storage-generated-documents.md) を参照してください。

### <a name="post-processing-of-imported-files"></a>ファイルをインポートした後の処理

電子申告 (ER) のインポート機能は、処理大砲のファイルの取得先として SharePoint のフォルダを使用しています。 前回までのリリースでは、処理されたファイルを管理する自動プロセスが実装されていませんでした。 たとえば、正常に処理されたファイルは SharePoint のソース フォルダーから自動的に削除され、他の場所に移動することができませんでした。 結果として、さらなる手作業が必要となり誤操作の潜在的原因となっていました。 この機能には処理済みのファイルを管理する機能が実装されており、処理終了後の動作を設定することができるようになります。 ERフォーマットの読み込みの設定を変更することで、次の動作を設定することができます。

正常に処理されたファイルのフォルダー
- 読み込み元の SharePoint フォルダからファイルを削除する。
- 処理済ファイルを別の SharePoint フォルダーに移動します
警告で処理されるファイルの場合
- 読み込み元の SharePoint フォルダにファイルを保持する。
- 処理済ファイルを別の SharePoint フォルダーに移動します
処理に失敗したファイル
- 読み込み元の SharePoint フォルダにファイルを保持する。
- 処理済ファイルを別の SharePoint フォルダーに移動します

### <a name="generate-documents-in-pdf-format-by-filling-in-pdf-templates"></a>PDFのテンプレートに入力することにより、PDF形式でドキュメントを生成を可能にします。

この機能では、レポートをPDF形式で生成するにあたって、入力可能なPDFドキュメントをテンプレートとして使用できます。 設計時に調整済みのERフォーマットにPDFをインポートすることで、入力が必要な項目が検出されERフォーマットに新たな要素が自動で生成されます。 ERフォーマット上に生成された要素にバインドを追加することで、PDFテンプレート上の必要項目に入力をすることが可能となります。 この機能を使用することで、ERフォーマットを設定して複数のPDFドキュメントを生成したうえで、自動的にそれら複数のファイルを1つの最終版PDFドキュメントに統合することも可能です。

## <a name="russian-features"></a>ロシア用の機能

### <a name="cash-flow-management"></a>キャッシュ フロー管理 

この機能によって、次のことが可能となります。
- キャッシュ フローを予測し、分析を行う
- 支払スケジュール仕訳帳を使用して支払を日次単位で管理する
- 会社の現金持高を管理する
- 集中管理方式で会社のキャッシュ フローを管理する

詳細については、「 [キャッシュ フローの管理 (ロシア) ](../../financials/localizations/rus-cash-flow.md) 」を参照してください。

### <a name="other-incomes-and-expenses-profit-tax-registers"></a>その他の収入/支出 収益税 の登録

次の税登録を使用できます。

- 現在の期間の収入
- 税経費
- 現在の期間の他の経費
- 現在の期間の未実現経費
- その他の未実現経費

### <a name="localization-of-process-industries"></a>Process Industries のローカライズ

以下2点での基本的なローカライズが使用可能です。
- すべての新しい総勘定元帳の転記に対応しています。
- 機能面においてプロセス産業とロシア国の関係性の共存を実現しています。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正
Finance and Operations 10.0 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://go.microsoft.com/fwlink/?linkid=2080156)を参照してください。 

## <a name="regulatory-updates"></a>規制の更新
Finance and Operations の規制の更新については、[ローカライズおよび規制機能 – 規制の更新](../../financials/localizations/regulatory-updates.md) を参照してください。 また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。

### <a name="platform-update-24"></a>プラットフォーム update 24
Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 には、プラットフォーム更新プログラム 24 が含まれています。 プラットフォーム更新プロフラム 24 については [Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能と変更された機能](whats-new-platform-update-24.md) を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。
