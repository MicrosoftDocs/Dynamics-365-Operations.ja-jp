---
title: 拡張可能なデータ セキュリティ ポリシー
description: この記事では、財務と運用アプリにおける拡張可能なデータ セキュリティ (XDS) ポリシーの概要を提供します。
author: Peakerbl
ms.date: 03/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: sericks
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 8139161ee1552599cd109ec111501c41e7060430
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881077"
---
# <a name="extensible-data-security-policies"></a>拡張可能なデータ セキュリティ ポリシー 
[!include [banner](../includes/banner.md)]

この記事では、財務と運用アプリにおける拡張可能なデータ セキュリティ (XDS) ポリシーの概要を提供します。 XDS を使用すると、開発者は、セキュリティ ポリシーに基づいてテーブル レコードへのアクセスを制限することにより、ロールベースのセキュリティを補うことができます。 ポリシー内のクエリにはフィルターが適用されます。また、そのフィルターの条件を満たすレコードだけが、制限されたテーブルからアクセスできるようになります。

## <a name="data-security-policy-components"></a>データ セキュリティ ポリシー コンポーネント

-   **制約付きテーブル**: データがフィルタ処理またはセキュリティ保護されているテーブル。 たとえば、顧客に基づく取引へのアクセスを保護するポリシーでは、**CustTrans** は制約されたテーブルの例になります。

-   **プライマリ テーブル**: 関連する制約付きテーブルの内容を保護するために使用されます。 次の例では、**CustTable** テーブルがプライマリ テーブルになります。
    プライマリ テーブルには、制約されたテーブルと明示的な関係である必要があります。

-   **ポリシー クエリ**: プライマリ テーブルの内容に対する範囲条件を使用して、制約を適用するテーブル コンテンツを保護するために使用されます。 範囲に含まれるレコードのみがアクセス可能になります。 この範囲は、顧客の特定の値に基づいている場合などに使用できます。

-   **コンテキスト** – ポリシーが適用される条件を制御します。
    主に 2 種類のコンテンツを利用できます。

    -   **ロール コンテキスト**: ユーザーが割り当てられているロールに基づきます。 ロール コンテキストには 2 つのサブオプションがあります。

        -   **RoleName** – セキュリティ ポリシーは、RoleName の値と等しいロールに割り当てられているアプリケーション ユーザーにのみ適用されることを示します。

        -   **RoleProperty** – この値は、**ContextString** プロパティと組み合わせて使用され、複数のロール コンテキストを指定します。 ポリシーの **ロール プロパティ** フィールドで定義されているコンテキスト文字列の値が、割り当てられたユーザー ロールの **ContextString** フィールドの値と同じである場合に適用されます。

    -   **アプリケーション コンテキスト**: XDS::SetContext API を使用しているアプリケーションによって設定されたコンテキスト文字列が、ポリシーの **コンテキスト文字列** フィールドで定義した値と同じである場合に適用されます。

        ![AOTXDS 概念モデル。](media/c74bc4ea12f084dfbaddb024685843e8.jpg)

アプリケーション オブジェクト ツリー (AOT) では、ポリシーとそのコンポーネントが **セキュリティ \> ポリシー** に基づいて表示されます。

## <a name="important-considerations"></a>重要な考慮事項

ポリシー クエリは、指定された制約付きテーブルを含む選択、更新、削除、および挿入の各操作において WHERE 句または ON 句に追加されます。 入念に設計され、テストされていない限り、ポリシー クエリはパフォーマンスに重要な影響を与える可能性があります。 したがって、拡張可能なデータ セキュリティ ポリシーを開発する場合は、必ず単純ですが、重要なガイドラインに従ってください。 詳細については、[拡張可能なデータ セキュリティ ポリシーの開発 (ホワイト ペーパー) [AX 2012]](/dynamicsax-2012/appuser-itpro/developing-extensible-data-security-policies-white-paper) の「拡張可能なデータ セキュリティ ポリシーの開発」を参照してください。

2 つ以上のセキュリティ ポリシーが適用されている場合は、各ポリシーに含まれるレコードの交差 (和集合ではない) のみが、アクセス可能なレコードとなります。 つまり、レコードへのアクセスを許可する前に、レコードが適用可能なすべてのセキュリティ ポリシーを満たす必要があります。

XDS は財務分析コードには対応しておらず、財務分析コード データで XDS を使用すると、データが破損する可能性があります。

## <a name="additional-resources"></a>追加リソース

ポリシーをデバッグする方法の詳細については、制限されたテーブルのチェーン、式に基づくテーブルの関係を含むより詳細なポリシーを作成し、これらのリソースを参照してください。

- [単純なセキュリティ ポリシーを作成する](create-simple-security-policy.md)

- [拡張可能なデータ セキュリティ ポリシーの開発 (ホワイト ペーパー) [AX 2012]](/dynamicsax-2012/appuser-itpro/developing-extensible-data-security-policies-white-paper)

- [拡張可能なデータ セキュリティの例 – Andre Arnaud De Calavon [ブログ]](https://dynamicspedia.com/tag/xds/)

- [D365FO - Alex Meyer [ブログ]での拡張可能なデータ セキュリティ (XDS) フレームワーク](https://alexdmeyer.com/2019/02/20/extensible-data-security-xds-framework-in-d365fo/)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
