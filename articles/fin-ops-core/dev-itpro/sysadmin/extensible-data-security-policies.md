---
title: 拡張可能なデータ セキュリティ ポリシー
description: このトピックでは、Finance and Operations アプリにおける拡張可能なデータ セキュリティ (XDS) ポリシーの概要を提供します。
author: Peakerbl
manager: AnnBe
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: sericks
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 639b0dbe4c1328fbf22628b50b2630651be7c7e2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686325"
---
# <a name="extensible-data-security-policies"></a>拡張可能なデータ セキュリティ ポリシー 
[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリにおける拡張可能なデータ セキュリティ (XDS) ポリシーの概要を提供します。 XDS を使用すると、開発者は、セキュリティ ポリシーに基づいてテーブル レコードへのアクセスを制限することにより、ロールベースのセキュリティを補うことができます。 ポリシー内のクエリにはフィルターが適用されます。また、そのフィルターの条件を満たすレコードだけが、制限されたテーブルからアクセスできるようになります。

## <a name="data-security-policy-components"></a>データ セキュリティ ポリシー コンポーネント

-   **制約付きテーブル**: データがフィルタ処理またはセキュリティ保護されているテーブル。 たとえば、顧客グループに基づく顧客へのアクセスを保護するポリシーでは、**CustTable** は制約されたテーブルになります。

-   **プライマリ テーブル**: 関連する制約付きテーブルの内容を保護するために使用されます。 上の例では、 **CustGroup** テーブルがプライマリ テーブルになります。
    プライマリ テーブルには、制約されたテーブルと明示的な関係である必要があります。

-   **ポリシー クエリ**: プライマリ テーブルの内容に対する範囲条件を使用して、制約を適用するテーブル コンテンツを保護するために使用されます。 範囲に含まれるレコードのみがアクセス可能になります。 この範囲は、顧客グループの特定の値に基づいている場合などに使用できます。

-   **コンテキスト** – ポリシーが適用される条件を制御します。
    主に 2 種類のコンテンツを利用できます。

    -   **ロール コンテキスト**: ユーザーが割り当てられているロールに基づきます。 ロール コンテキストには 2 つのサブオプションがあります。

        -   **RoleName** – セキュリティ ポリシーは、RoleName の値と等しいロールに割り当てられているアプリケーション ユーザーにのみ適用されることを示します。

        -   **RoleProperty** – この値は、**ContextString** プロパティと組み合わせて使用され、複数のロール コンテキストを指定します。 ポリシーの **ロール プロパティ** フィールドで定義されているコンテキスト文字列の値が、割り当てられたユーザー ロールの **ContextString** フィールドの値と同じである場合に適用されます。

    -   **アプリケーション コンテキスト**: XDS::SetContext API を使用しているアプリケーションによって設定されたコンテキスト文字列が、ポリシーの **コンテキスト文字列** フィールドで定義した値と同じである場合に適用されます。

        ![AOTXDS 概念モデル](media/c74bc4ea12f084dfbaddb024685843e8.jpg)

アプリケーション オブジェクト ツリー (AOT) では、ポリシーとそのコンポーネントが **セキュリティ \> ポリシー** に基づいて表示されます。

## <a name="important-considerations"></a>重要な考慮事項

ポリシー クエリは、指定された制約付きテーブルを含む選択、更新、削除、および挿入の各操作において WHERE 句または ON 句に追加されます。 入念に設計され、テストされていない限り、ポリシー クエリはパフォーマンスに重要な影響を与える可能性があります。 したがって、拡張可能なデータ セキュリティ ポリシーを開発する場合は、必ず単純ですが、重要なガイドラインに従ってください。 詳細については、[拡張可能なデータ セキュリティ ポリシーの開発 (ホワイト ペーパー) [AX 2012]](https://technet.microsoft.com/library/hh272862.aspx) の「拡張可能なデータ セキュリティ ポリシーの開発」セクションを参照してください。

2 つ以上のセキュリティ ポリシーが適用されている場合は、各ポリシーに含まれるレコードの交差 (和集合ではない) のみが、アクセス可能なレコードとなります。 つまり、レコードへのアクセスを許可する前に、レコードが適用可能なすべてのセキュリティ ポリシーを満たす必要があります。

## <a name="additional-resources"></a>追加リソース

ポリシーをデバッグする方法の詳細については、制限されたテーブルのチェーン、式に基づくテーブルの関係を含むより詳細なポリシーを作成し、これらのリソースを参照してください。

- [単純なセキュリティ ポリシーを作成する](create-simple-security-policy.md)

- [拡張可能なデータ セキュリティ ポリシーの開発 (ホワイト ペーパー) [AX 2012]](https://technet.microsoft.com/library/hh272862.aspx)

- [拡張可能なデータ セキュリティを使用した分析コード値ごとのデータの保護 (ホワイト ペーパー) [AX 2012]](https://technet.microsoft.com/library/hh335188.aspx)

- [拡張可能なデータ セキュリティの例 – Andre Arnaud De Calavon [ブログ]](https://dynamicspedia.com/tag/xds/)

- [D365FO での拡張可能なデータ セキュリティ (XDS) フレームワーク - Alex Meyer [ブログ]](https://alexdmeyer.com/2019/02/20/extensible-data-security-xds-framework-in-d365fo/)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]