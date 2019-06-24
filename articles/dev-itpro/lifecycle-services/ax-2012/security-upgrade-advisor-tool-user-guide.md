---
title: セキュリティ アップグレード アドバイザー ツールのユーザー ガイド
description: Microsoft Dynamics AX Security Upgrade Advisor Tool を使用すると、以前のバージョンの Microsoft Dynamics AX から Microsoft Dynamics AX 2012 にセキュリティ設定をアップグレードするプロセスを簡略化できます。
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 30061
ms.assetid: fda4d8e9-79a2-4ee2-831e-a90a9df2d980
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: 6d5545580168dcd8fb335b6ebd4ac7ace11d83e2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555252"
---
# <a name="security-upgrade-advisor-tool-user-guide"></a>セキュリティ アップグレード アドバイザー ツールのユーザー ガイド

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics AX Security Upgrade Advisor Tool を使用すると、以前のバージョンの Microsoft Dynamics AX から Microsoft Dynamics AX 2012 にセキュリティ設定をアップグレードするプロセスを簡略化できます。 

> [!NOTE]
> これは、予備的なプレリリース ドキュメントで、予告なしに変更される場合があります。 ここで提供されている情報の正確さは保障されていません。

セキュリティ アップグレード アドバイザー ツールは、システム間でエントリ ポイントとアクセス許可を比較し、特定のロールのために使用できる一致する特権の一覧を生成します。 ロールから権限へのマッピングは、以前のバージョンの Microsoft Dynamics AX システムでの、ユーザー グループからアクセスへの正しいマッピングに基づいています。 このツールは、セキュリティ設定をアップグレードするためのもので、ワンクリック ソリューションではありません。 開発者は、変更を行う前に各提案を慎重に検討することをお勧めします。 生成される提案のリストは、次の基準に基づいています。

1.  エントリ ポイントの名前、タイプ、アクセス権は、以前のバージョンの Microsoft Dynamics AX と Microsoft Dynamics AX 2012 との間で正確に一致します。
2.  エントリ ポイントの名前とタイプは完全に一致しています。 ただし、アクセス権に関しては、完全な一致が見つからない場合、類似した一致候補が生成されます。 以前のバージョンの Microsoft Dynamics AX および Microsoft Dynamics AX 2012 の両方でビューよりも大きいアクセス権は、潜在的な一致とみなされます。

## <a name="assumptions"></a>前提
このツールを使用する前に、次の前提条件を満たす必要があります。

-   Microsoft Dynamics AX および Microsoft Dynamics AX 2012 の以前のバージョンの開発環境を使い慣れています。
-   Microsoft Dynamics AX および Microsoft Dynamics AX 2012 の以前のバージョンのセキュリティ モデルを使い慣れています。
-   Microsoft Dynamics AX の開発者権限を持っている場合、アプリケーション オブジェクト ツリー (AOT) からツールを実行できるようにします。
-   コードのアップグレードおよびデータのアップグレードが完了しました。 セキュリティ アップグレード アドバイザー ツールはいつでも実行できますが、コード アップグレードの後に実行すると、コンポーネントを以前のバージョンの Microsoft Dynamics AX から持ち越すことができます。

## <a name="install-the-tool"></a>ツールのインストール
1.  **SecurityUpgradeAdvisorTool.msi** を実行して**インストール ウィザード**を開きます。
2.  使用許諾契約書に同意し、**インストール**をクリックします。
3.  **完了**をクリックしてインストールを完了します。 **インストール ウィザード**の実行が完了すると、ファイルは、x64 システム - %ProgramFiles(x86)%MicrosoftSecurity アップグレード アドバイザー Toolx32 システム - %ProgramFiles%MicrosoftSecurity アップグレード アドバイザー ツールで使用可能です

## <a name="before-running-the-tool"></a>ツールを実行する前に
このツールを実行する前に、以下の点を考慮する必要があります。

-   ソース管理: ソース管理が有効な場合、ツールはロールと特権の生成をサポートしません。
-   モデル: モデルですべてのセキュリティ アップグレード タスクを実行します。 これにより、新しく生成された設定を新しい環境に柔軟にエクスポートできます。 また、これにより、設定をクリーンアップおよび再生成する必要がある場合に、全体の設定を削除することもできます。
-   テスト: ツールは、Microsoft Dynamics AX の以前のバージョンからのセキュリティ設定に基づいてセキュリティ コンポーネントを生成します。 各設定の確認、調整、およびテストを繰り返して、生成された設定が目的の設定になっていることを確認することをお勧めします。

## <a name="running-the-tool"></a>ツールを実行中
次の手順では、セキュリティ アップグレード アドバイザー ツールの実行時に従う必要があるプロセスについて説明します。

### <a name="export-security-settings-from-an-environment-running-an-earlier-version-of-microsoft-dynamics-ax"></a>Microsoft Dynamics AX の以前のバージョンを実行している環境から、セキュリティ設定をエクスポート

1.  Microsoft Dynamics AX の以前のバージョンを実行している環境で、次の XPO をインポートします。**Job\_ExportSecuritySettingsBulk.xpo**。
2.  X++ ジョブ **ExportSecuritySettingsBuild** を実行します。
3.  メッセージが表示されたら、保存するファイルの名前を入力します。
4.  ファイルを既知の場所にエクスポートして、後で取得します。

### <a name="run-the-security-upgrade-wizard-in-microsoft-dynamics-ax-2012"></a>Microsoft Dynamics AX 2012 でセキュリティ アップグレード ウィザードを実行

ウィザードの出力は、指定した接頭語で名前が付けられた AOT のカスタム ロールです。 ユーザーはこれらのロールに自動的に割り当てられません。 ロールが生成されると、各ユーザーにロールを手動で割り当てる必要があります。 **次へ**をクリックすると、ウィザードの各ステップを実行します。 **キャンセル**をクリックすると、ウィザードが閉じます。

1. 使用している Application Object Server (AOS) のインスタンスに接続されているクライアント接続を排除します。 詳細については、[AOS からユーザーを排除](http://technet.microsoft.com/library/d19bd816-cd9e-423a-94c7-aceb946baa30(AX.60).aspx) を参照してください。
2. **管理ツール** &gt; **サービス**で、**Microsoft Dynamics AX Object Server 6.0** サービスを停止します。
3. Windows PowerShell または AXUtil を使用して、**SecurityUpgradeAdvisorTool.axmodel** モデルを Microsoft Dynamics AX 2012 AOT にインポートします。

       Install-AXModel -File SecurityUpgradeAdvisorTool.axmodel -Details

   詳細については、「[方法: モデルのエクスポートとインポート](http://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx)」を参照してください。

4. **Microsoft Dynamics AX Object Server 6.0** サービスを開始します。
5. Security Upgrade Advisor プロジェクトを開いて、<strong>フォーム</strong>&gt;<strong>SecurityUpgradeWizard</strong> フォームを開きます。
  > [!IMPORTANT]
  > プロジェクトをコンパイルして、AOT の オブジェクト グループ **UpgradeAdvisorTool** および **PrivelegeGenerationTool** にあるすべてのテーブルを同期します。
6. **次へ**をクリックし、**ステップ１インポートの設定**ページを開きます。 このステップでは、以前のバージョンの Microsoft Dynamics AX からエクスポートされたセキュリティ情報の .xml ファイルを Microsoft Dynamics AX 2012 の一時テーブルにインポートします。 このステップでは、前のセクションで生成されたファイルを使用します。
7. **次へ**をクリックし、**ステップ 2 権限の一致を検索**ページを開きます。 このステップでは、既存のセキュリティ設定を繰り返し、Microsoft Dynamics AX 2012 で一致するエントリ ポイントとアクセス許可を検出します。
8. **次へ**をクリックし、**ステップ 3 ユーザー グループをカスタムロールにマップ** ページを開きます。 このステップでは、検出された権限の新しいカスタム ロール マッピングが生成されます。
9. **次へ**をクリックし、**ステップ 4 セキュリティ アップグレード提案のエクスポート** ページを開きます。 このステップは、すべてのマッピングを一時テーブルにエクスポートします。
10. **次へ**をクリックし、**ステップ 5 セキュリティ アップグレード提案**ページを開きます。 このウィザードのページには推奨されるセキュリティ マッピングが表示されます。 
  > [!IMPORTANT]
  > 追加の分析のアップグレードの提案をエクスポートすることを強くお勧めします。 Ctrl + T を押すことで、追加分析のためにデータを Microsoft Excel にコピーして貼り付けることができます。 推奨される設定を分析する方法の詳細については、次のセクションを参照してください。
11. セキュリティ アップグレード提案の解析中に **NoMatchingPrivilege** ステータスを持つ複数の品目がある場合、権限生成ツールを実行できます。 **特権の生成**をクリックします。
12. **次へ**をクリックし、**ステップ 6 カスタム ロール生成オプションの指定**ページを開きます。 この手順では、AOT 内でのロールを生成するためのオプションを指定できます。
    -   **類似**ステータスに一致する特権を使用し、カスタム ロールに追加するには、カスタム ロールで**類似する一致を含める**を選択します。
    -   **カスタム ロール名の省略可能な接頭語**フィールドに、新しいロールの接頭語を入力します。 AOT でのロールを後で簡単に識別するのに役立つ接頭語を使用することをお勧めします。 Microsoft Dynamics AX 2009 システムにドメインがある場合は、別のドメインにある類似したユーザー グループの名前を区別するために、ロールの前にドメイン名を付けることができます。

13. **完了**をクリックし、ウィザードを終了します。

ウィザードの実行が完了したら、推奨されるセキュリティ マッピングに基づいたカスタムのロールを AOT 内で使用できます。 生成されたのカスタム ロールを確認し、反復テストと調整プロセスに従ってセキュリティ設定を微調整することを強くお勧めします。

## <a name="analyzing-upgrade-suggestions"></a>アップグレード提案の分析
セキュリティ アップグレード アドバイザー ツールの手順 5 で生成される結果は、すべてのロール、エントリポイント、権限、一致する権限の一覧です。 これは次の列が含まれています。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>列</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span class="ui">ドメイン</span></td>
<td>Microsoft Dynamics AX 2009 からインポートされたドメイン名。</td>
</tr>
<tr class="even">
<td><span class="ui">役割</span></td>
<td>Microsoft Dynamics AX 2009 からインポートされたユーザー グループ名。 列内のデータは、特殊文字を削除するようにフォーマットされています。</td>
</tr>
<tr class="odd">
<td><span class="ui">権限</span></td>
<td>Microsoft Dynamics AX 2012 での一致する権限。 この列には、<strong><span class="ui">ステータス</span></strong>列の値が<strong><span class="ui">完全一致</span></strong>または<strong><span class="ui">類似</span></strong>の場合にのみ値が含まれます。</td>
</tr>
<tr class="even">
<td><span class="ui">エントリ ポイント 名</span></td>
<td>Microsoft Dynamics AX 2009 からインポートされたエントリ ポイント名。</td>
</tr>
<tr class="odd">
<td><span class="ui">新規エントリ ポイント名</span></td>
<td>エントリ ポイントが以前のバージョンの Microsoft Dynamics AX から Microsoft Dynamics AX 2012 に変更されている場合、スクリプトは自動的に新しいエントリ ポイント名に基づく特権をマップし、新しい名前でこの列に値を設定します。</td>
</tr>
<tr class="even">
<td><span class="ui">エントリ ポイント タイプ</span></td>
<td>エントリ ポイントのタイプ</td>
</tr>
<tr class="odd">
<td><span class="ui">エントリ ポイント アクセス権限</span></td>
<td>Microsoft DynamicsAX 2012 で一致するエントリ ポイントのアクセス許可。 この列には、<strong><span class="ui">ステータス</span></strong>列の値が<strong><span class="ui">完全一致</span></strong>または<strong><span class="ui">類似</span></strong>の場合にのみ値が含まれます。</td>
</tr>
<tr class="even">
<td><span class="ui">エントリ ポイント 旧アクセス権限</span></td>
<td>Microsoft Dynamics AX 2009 で設定されたエントリポイントの権限。 この列は参照用に追加されています。</td>
</tr>
<tr class="odd">
<td><span class="ui">ステータス</span></td>
<td>各エントリ ポイントの状態が一致します。 このツールでは、次のステータスが生成されます。
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span class="ui">正確</span></td>
<td>エントリポイント、タイプ、アクセス権は、Microsoft Dynamics AX 2012 の権限と完全に一致します。 提案された特権は、Microsoft Dynamics AX 2012 の同様のセキュリティ設定の指定された役割で使用できます。</td>
</tr>
<tr class="even">
<td><span class="ui">類似</span></td>
<td>エントリ ポイントとタイプは正確に一致しますが、アクセス権の完全一致は見つかりませんでした。 ただし、古いアクセス権および新しいアクセス権の両方に<strong>表示</strong>より大きいアクセス許可があるため、一致する可能性があります。
<table>
<thead>
<tr class="header">
<th><strong>重要</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>開発者と管理者はこれらの行を確認し、提案された権限が目的のセキュリティ結果と一致することを確認する必要があります。</td>
</tr>
</tbody>
</table></td>
</tr>
<tr class="odd">
<td><span class="ui">NoEntryPoint</span></td>
<td>以前のバージョンの Microsoft Dynamics AX と Microsoft Dynamics AX 2012 には、一致するエントリ ポイントとタイプがありませんでした。 見つからない品目には、マッピングの手動エントリ ポイントを実行する必要があります。</td>
</tr>
<tr class="even">
<td><span class="ui">NoMatchingPrivilege</span></td>
<td>Microsoft Dynamics AX 2012 にてエントリ ポイントが見つかった場合でも、アクセス権に任意の条件が一致しませんでした。 アクセス権限の手動マッピングが必要になるか、権限生成ツールを使用して権限を生成することができます。</td>
</tr>
<tr class="odd">
<td><span class="ui">非推奨</span></td>
<td>Microsoft Dynamics AX 2012 からエントリ ポイントが削除されました。</td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

## <a name="privilege-generation-tool"></a>特権生成ツール
特権生成ツールは、セキュリティ アップグレード アドバイザー ツールに組み込まれています。 カスタム エントリ ポイントに特権がなく、関連するアクセス権が定義されていないシナリオが多数あります。 ベスト プラクティスは、権限をエントリ ポイントに関連付けることをお勧めします。 権限が事前に定義されていない場合、権限生成ツールはアップグレード プロセス中に自動的に権限を生成します。 状態が **NoMatchingPrivilege** のすべてのエントリ ポイントに対して権限を生成するには、次の手順を使用します。

1.  セキュリティ アップグレード ツールから、**手順 5 セキュリティ アップグレード提案ページで、権限の生成をクリックします** 

       - または -

       AOT からの特権生成ツール フォームを、**PrivilegeGenerationTool** &gt; **フォーム** &gt; **SecurityUpgradePrivilegeGenerator** で開きます。
       
2.  **ステップ １: 特権生成ウィザード**ページで、**次へ**をクリックし、ウィザードを開始します。
3.  手順 2 では、追加する省略可能な接頭語を指定し、生成された権限の名前に追加してから、**次へ**をクリックします。
4.  手順 3 では、生成できるすべての特権が一覧表示されます。 生成する特権ごとに **作成** を選択し、**次へ** をクリックします。
5.  権限の生成が完了した後に、**完了**をクリックしてウィザードを閉じます。
6.  AOT で、**セキュリティ**&gt;**権限**を確認して権限が正常に生成されたことを確認します。
7.  新しい権限を表示するように AOT を更新し、コンパイルして正しく生成されていることを確認します。
8.  セキュリティ アップグレード アドバイザー ツールをもう一度実行します。

> [!IMPORTANT]
> Microsoft Dynamics AX の以前のバージョンに **SysUtilElementsLog** メニュー項目がある場合は、特権が生成されると、コンパイル エラーが表示されます。 **SysUtilElementsLog** メニュー項目のタイプが Microsoft Dynamics AX 2012 での表示に変更されました。 
> **回避策:** この問題を回避するには、タイプを**表示**に変更し、権限に名前を再割り当てしてください。 |

## <a name="frequently-asked-questions"></a>よく寄せられる質問
### <a name="can-you-automatically-generate-role-definitions-from-excel"></a>Excel からロール定義を自動的に生成できますか。

一連番号 Excel のスプレッドシートを変更し、それらの設定を使用してロールを生成することはできません。 ただし、ツールを使用して、カスタム ロールおよび特権を生成できます。

### <a name="what-happens-to-the-custom-menu-items-that-were-used-in-the-earlier-versions-of-microsoft-dynamics-ax"></a>Microsoft Dynamics AX の以前のバージョンで使用されていたカスタム メニュー項目はどうなったでしょうか？

コードのアップグレードが完了したシステムでこのツールを実行するとき、Microsoft Dynamics AX 2012 システムでメニュー項目と一致するものを検索します。 ただし、それらに対する権限はありません。 適用可能と思われる場合は、新しい権限を作成する必要があります。

### <a name="does-the-tool-consider-other-artifacts-such-as-tables-and-forms"></a>ツールは、テーブルやフォームなどの他のコンポーネントを考慮しますか。

いいえ、このツールでは、メニュー項目などのエントリ ポイントのみが考慮されます。 Microsoft Dynamics AX 2012 のセキュリティ モデルでは、権限がアーティファクトへのアクセスを維持するために使用されます。

### <a name="are-the-user-groups-mapped-for-all-the-domains"></a>ユーザー グループは、すべてのドメインにマップされていますか。

はい。 結果は各ドメインとユーザーグループです。 Microsoft Dynamics AX 2012 の組織構造に基づいて、Microsoft Dynamics AX 2012 でロールを作成するユーザー グループとドメインの組み合わせを決定します。

### <a name="are-users-moved-as-part-of-the-security-upgrade"></a>ユーザーはセキュリティ アップグレードの一部として移動しますか。

ユーザー情報は保存または移動されません。 Microsoft Dynamics AX 2012 でロールを作成した後、ユーザー ロール マッピングを手動で作成する必要があります。

### <a name="are-record-level-security-settings-moved-as-part-of-the-security-upgrade"></a>レコード レベルのセキュリティ設定はセキュリティ アップグレードの一部として移動しますか。

アップグレードされるレコード レベルのセキュリティ (RLS) ルールはありません。 Microsoft Dynamics AX 2012 には、拡張可能なデータ セキュリティ (XDS) と呼ばれる新しくより豊富なデータのセキュリティ メカニズムがあります。 新しい XDS ポリシーを業務要件に基づいて作成することをお勧めします。

### <a name="what-are-the-next-steps-to-complete-the-security-upgrade"></a>セキュリティのアップグレードを完了するための次の手順

結果を使用して Excel スプレッドシートが生成された後は、ツールでロール生成と権限生成の機能を使用して、ロールと権限を自動的に作成することができます。 次に、ユーザーをそれらの役割に割り当ててシステムをテストし、アクセス権と公開されている機能が正確であることを検証します。



