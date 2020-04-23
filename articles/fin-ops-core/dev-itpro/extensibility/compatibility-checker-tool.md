---
title: 互換性チェック ツール
description: このトピックでは、メタデータの互換性を破る変更を検索して報告する互換性チェックツールについて説明します。
author: smithanataraj
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2020-03-26
ms.dyn365.ops.version: Platform update 34
ms.openlocfilehash: e3e8c4d225ccc168993869d9e7db6d5cc4ed3f4b
ms.sourcegitcommit: dca6ac616b901f33ad278dfd9c7ef55b7c898840
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/03/2020
ms.locfileid: "3225513"
---
# <a name="compatibility-checker-tool"></a>互換性チェック ツール

[!include [banner](../includes/banner.md)]

互換性チェックツールを使用すると、指定されたベースライ ンリリースまたは更新に対して、メタデータの互換性に影響する変更を検出できます。 このように下位互換性を確保します。 Microsoft では、メタデータの互換性確保にこのツールを使用します。

互換性チェックツールは、プラットフォーム更新プログラム 34 の開発ツールの 1 つとして使用できます。 この方法を使用すると、更新プログラムを顧客にインストール、プッシュ配信する前に、ソリューションに旧版のリリースとの下位互換性を持たせることができます。

## <a name="what-the-tool-detects"></a>ツールによって検出される内容

このツールでは、現在のバージョンのメタデータとベースライン バージョンのメタデータが比較されます。 Microsoft が破損を判断してツールに追加したメタデータの変更を検出して報告します。

ツールが検出する互換性を破る変更のリストについては、このトピックで後述する[ツールが検出する互換性を破る変更のリスト](#list-of-breaking-changes-detected-by-the-tool)のセクションを参照してください。

> [!NOTE]
> + このトピックの一覧には、ツールが検出できる互換性に影響するすべての変更が含まれているわけではありません。
> + このツールでは、互換性に影響するすべての変更を検出できるわけではありません。

## <a name="what-the-tool-doesnt-detect"></a>ツールで検出されないもの

このツールでは、データの比較によって識別できる、互換性に影響する変更のみが検出されます。 たとえば、次のような場合に発生する可能性のある、互換性に影響する変更は検出されません。

+ 保護されたメソッドまたはパブリック メソッドへの参照が削除されます。
+ メソッドの責任が変更されます。

## <a name="using-the-tool"></a>ツールの使用

このツールを使用すると、新しいバージョンが置き換えるバージョンに対して持つメタデータの互換性の問題を検出することができます。 Microsoft は、このツールを使用して、新たな月次更新が前回の月次更新と比較してどのような互換性に影響する変更があったかを検出します。

### <a name="usage"></a>使用状況

```console
CompatibilityChecker.exe -BaselineDirectory=\<Path to baseline metadata\> -CurrentDirectory=\<Path to current metadata\> -ModuleName=\<Module name\> -OutputFile=\<Output file path\> -LogFile=\<Log file path\>
```

### <a name="example"></a>例

```console
CompatibilityChecker.exe -BaselineDirectory="\\servername\archive\Build1\BaselineMetadata" -CurrentDirectory="E:\\MyCode\\retail\\amd64\\BaselineMetadata" -ModuleName="Directory"
-OutputFile="E:\\Logs\\Directory\\Diagnostics.xml" -LogFile="E:\\Logs\\Directory\\Checkerlog.txt"
```

### <a name="description"></a>説明

このツールは、現在のメタデータと指定されたベースラインのメタデータを比較することで、互換性に影響する変更を識別します。

次のパスを指定する必要があります。

+ **BaselineDirectory** – ベースラインとなるメタデータのパス。
+ **CurrentDirectory** – 現在の (新しい) メタデータのパス。
+ **OutputFile** – 互換性に影響する変更の一覧を含むファイルのパス。

次のルールが適用されます。

+ ツールを実行する前に、現在のメタデータをコンパイルする必要があります。
+ *OutputFile* – ファイルには、ツールが識別した互換性に影響する変更のリストが含まれています。
+ *BaselineDirectory* ディレクトリが存在し、指定されたモジュールとその依存関係 (モジュールに依存関係がある場合) のメタデータが必要です。
+ *BaselineDirectory* および *currentdirectory* のメタデータパスには、 *staticmetadata* のメタデータを含める必要があります。 このメタデータは、指定したパスの **staticmetadata** という名前のフォルダに存在する必要があります。
+ モデルの無視リストにエントリを追加することで、ツールが識別したすべての互換性に影響する変更を抑制することができます。 このファイルは、モデルの **AxIgnoreDiagnosticList** フォルダに存在します。

## <a name="list-of-breaking-changes-detected-by-the-tool"></a>ツールが検出した互換性に影響のある変更の一覧

> [!NOTE]
> メタデータの互換性の変更は、ツールにて互換性に影響ありとして定義されている場合にのみ、互換性に影響のある変更として識別されます。

### <a name="class-members"></a>クラス メンバー

+ **保護されたクラス メンバまたはパブリック クラス メンバのアクセス モディファイアの変更 (メンバを読み取り専用にすることも含む)** – コンシューマーは、フィールドからの読み取りや、フィールドへの値の割り当てを行っている場合があります。
+ **パブリックまたは保護されたクラス レベルのメンバーを削除するか名前を変更する** – ユーザーは、拡張クラスでこれらのメンバーを使用している可能性があります。

### <a name="methods"></a>メソッド

+ **保護メソッドまたはパブリック メソッド** のメソッドシグネチャを変更すると、メソッドのラッパーと呼び出し元が破損します。
+ **保護メソッドまたはパブリック メソッドを使用しない** – コンシューマーは、メソッドをラップまたは上書きする場合があります。

### <a name="classes-and-interfaces"></a>クラスおよびインターフェイス

+ **クラスに最終化する** – ユーザーが派生タイプを作成した可能性があります。
+ **クラスの抽象化** – コンシューマーがクラスのインスタンスを作成している場合があります。
+ **クラスに抽象メソッドを追加する**: ユーザーは、派生タイプを作成した可能性があります。
+ **メソッドをインターフェイスに追加する**: 消費者は、独自の種類でインターフェイスを実装した可能性があります。
+ **パブリック クラスを古い形式にし、クラスのインスタンス化を停止する**: ユーザーは、インスタンス メソッドをオーバーライド、折り返し、またはサブスクライブしている可能性があります。

### <a name="delegates"></a>委任

+ **シグネチャにおける変更** – ユーザーは、動的に登録をしている場合があります。

### <a name="tables"></a>テーブル

次のいずれかの変更を行うと、テーブルの拡張子とテーブルのフィールドに対するテーブル参照が壊れることになります。

+ テーブル フィールド、フィールド グループ、インデックス、テーブルのマッピング、テーブルの関連付けを削除または名前変更する
+ これらテーブルのプロパティ変更: **Extends**、**suportinheritance**、**TableType**、**SaveDataPerCompany**、**SaveDataPerPartition**
+ これらのテーブル フィールドのプロパティの変更: **ExtendedDataType**、**Scale**、**文字列サイズ**
+ 次のテーブル インデックス プロパティを変更する：**AllowDuplicates.No** または **indextype**

### <a name="forms"></a>フォーム

次のいずれかの変更を行うと、コントロールまたはメソッドを参照するフォームの拡張機能が解除されます。

+ フォーム コントロール、フォーム データソース、フォーム データソース フィールドの削除または名前の変更。
+ メソッドに対して中断するすべての変更は、フォーム メソッドについても中断されます。

### <a name="enumerations-enums"></a>列挙 (列挙)

+ 次のプロパティの変更：**IsExtensible** または **Value**

### <a name="extended-data-types-edts"></a>拡張データ型 (EDTs)

+ これらプロパティの変更：**Extends**、**EnumType**、**Scale**

### <a name="entities"></a>エンティティ

+ テーブルに対して中断するすべての変更は、エンティティについても中断されます。
+ パブリック エンティティの名前変更。

### <a name="labels"></a>ラベル (複数)

+ **ラベルの変更または削除** – ユーザーがラベル テキストと渡されたパラメータの現在のコンテキストでラベルを使用している可能性があります。 既存のラベルを変更するのではなく、新しいラベルを追加することを推奨します。

### <a name="application-elements"></a>申請の要素

+ **要素を削除する** – ユーザーは、要素の存在にコンパイル時の依存関係を持っている可能性があります。
