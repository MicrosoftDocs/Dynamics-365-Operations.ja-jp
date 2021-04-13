---
ms.openlocfilehash: 5edfe6575bb28800f4554ad8c7401d7bc4e6915c
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555353"
---
<span data-ttu-id="07021-101">開発環境から標準ユーザー承認テスト (UAT) まで準備されたデータベース、または UAT 環境から前回エクスポートしたデータベースをインポートするには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="07021-101">To import a database that is prepared from a developer environment to a standard user acceptance test (UAT), or a database previously exported from a UAT environment, follow the steps outlined below:</span></span>

1. <span data-ttu-id="07021-102">ターゲット サンドボックスの **環境詳細** ページを開き、 メニュー オプションから **管理** > **データベースの移動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07021-102">Go to your target sandbox **Environment Details** page, and select the **Maintain** > **Move database** menu option.</span></span>
2. <span data-ttu-id="07021-103">**データベースのインポート** を選択し、資産ライブラリからソース データベースのバックアップ (.bacpac形式) ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="07021-103">Select **Import database** and choose your source database backup (.bacpac format) file from the Asset Library.</span></span>
3. <span data-ttu-id="07021-104">警告に注意してください。</span><span class="sxs-lookup"><span data-stu-id="07021-104">Note the warnings.</span></span> <span data-ttu-id="07021-105">バックアップ ファイルからクリーンアップされたデータ要素の一覧を確認します。</span><span class="sxs-lookup"><span data-stu-id="07021-105">Review the list of data elements that are cleaned up from the backup file.</span></span>
4. <span data-ttu-id="07021-106">インポート操作をすぐに開始します。</span><span class="sxs-lookup"><span data-stu-id="07021-106">The import operation will begin immediately.</span></span>

> [!NOTE]
> <span data-ttu-id="07021-107">管理者ユーザー、およびその他の内部サービス ユーザー アカウントを除くすべてのユーザーはインポート後に使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="07021-107">All users except the Admin user and other internal service user accounts will be unavailable after import.</span></span> <span data-ttu-id="07021-108">そのため、管理者ユーザーは他のユーザーがシステムに復帰する前にデータの削除や難読化することができます。</span><span class="sxs-lookup"><span data-stu-id="07021-108">Therefore, the Admin user can delete or obfuscate data before other users are allowed back into the system.</span></span>

<span data-ttu-id="07021-109">データベース バックアップ (.bacpac) ファイルをダウンロードした後、データベースを開発環境にインポートするには、レベル 1 環境の手動インポート操作の開始が可能です。</span><span class="sxs-lookup"><span data-stu-id="07021-109">To import a database to a developer environment after you've downloaded a database backup (.bacpac) file, you can begin the manual import operation on your Tier 1 environment.</span></span> <span data-ttu-id="07021-110">データベースをインポートするときは、これらのガイドラインに従うことお勧めします。</span><span class="sxs-lookup"><span data-stu-id="07021-110">When you import the database, we recommend that you follow these guidelines:</span></span>

- <span data-ttu-id="07021-111">必要な場合は、後で戻すことができるように、既存の AxDB データベースのコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="07021-111">Keep a copy of the existing AxDB database, so that you can revert to it later if needed.</span></span>
- <span data-ttu-id="07021-112">**AxDB\_fromProd** などの新しい名前の下に新しいデータベースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="07021-112">Import the new database under a new name, such as **AxDB\_fromProd**.</span></span>

<span data-ttu-id="07021-113">最良のパフォーマンスを確実にするためには、\*.bacpac ファイルをインポート元のコンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="07021-113">To ensure the best performance, copy the \*.bacpac file to the local computer that you're importing from.</span></span> <span data-ttu-id="07021-114">sqlpackage .NET Core for Windows を [Get sqlpackage .NET Core for Windows](https://docs.microsoft.com/sql/tools/sqlpackage-download?view=sql-server-ver15#get-sqlpackage-net-core-for-windows) からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="07021-114">Download sqlpackage .NET Core for Windows from [Get sqlpackage .NET Core for Windows](https://docs.microsoft.com/sql/tools/sqlpackage-download?view=sql-server-ver15#get-sqlpackage-net-core-for-windows).</span></span> <span data-ttu-id="07021-115">**コマンド プロンプト** ウィンドウを開き、sqlpackage .NET Core フォルダーから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="07021-115">Open a **Command Prompt** window, and run the following commands from the sqlpackage .NET Core folder.</span></span>

```

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:localhost /tdn:<target database name> /p:CommandTimeout=1200
```

<span data-ttu-id="07021-116">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="07021-116">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="07021-117">**tsn (ターゲット サーバー名)** – インポートする Microsoft SQL Server インスタンスの名前。</span><span class="sxs-lookup"><span data-stu-id="07021-117">**tsn (target server name)** – The name of the Microsoft SQL Server instance to import into.</span></span>
- <span data-ttu-id="07021-118">**tdn(ターゲット データベース名)** – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="07021-118">**tdn (target database name)** – The name of the database to import into.</span></span> <span data-ttu-id="07021-119">データベースが既に存在していては **いけません**。</span><span class="sxs-lookup"><span data-stu-id="07021-119">The database should **not** already exist.</span></span>
- <span data-ttu-id="07021-120">**sf(ソース ファイル)** – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="07021-120">**sf (source file)** – The path and name of the file to import from.</span></span>

> [!NOTE]
> <span data-ttu-id="07021-121">インポート中に、ユーザー名およびパスワードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="07021-121">During import, the user name and password aren't required.</span></span> <span data-ttu-id="07021-122">既定では、SQL Server は、現在サインインしているユーザーに対して Microsoft Windows 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="07021-122">By default, SQL Server uses Microsoft Windows authentication for the user who is currently signed in.</span></span>

<span data-ttu-id="07021-123">レベル 1 の環境に手動インポート処理を実行する方法については、[データベースのインポート](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/database/dbmovement-scenario-exportuat#import-the-database) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07021-123">For information about how to complete the manual import operations into a Tier 1 environment, see [Import the database](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/database/dbmovement-scenario-exportuat#import-the-database).</span></span> 
