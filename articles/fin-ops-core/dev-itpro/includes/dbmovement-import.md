<span data-ttu-id="ab613-101">開発環境から標準ユーザー承認テスト (UAT) まで準備されたデータベース、または UAT 環境から前回エクスポートしたデータベースをインポートするには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="ab613-101">To import a database that is prepared from a developer environment to a standard user acceptance test (UAT), or a database previously exported from a UAT environment, follow the steps outlined below:</span></span>

1. <span data-ttu-id="ab613-102">ターゲット サンドボックスの **環境詳細** ページを開き、 メニュー オプションから **管理** > **データベースの移動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ab613-102">Go to your target sandbox **Environment Details** page, and select the **Maintain** > **Move database** menu option.</span></span>
2. <span data-ttu-id="ab613-103">**データベースのインポート**を選択し、資産ライブラリからソース データベースのバックアップ (.bacpac形式) ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ab613-103">Select **Import database** and choose your source database backup (.bacpac format) file from the Asset Library.</span></span>
3. <span data-ttu-id="ab613-104">警告に注意してください。</span><span class="sxs-lookup"><span data-stu-id="ab613-104">Note the warnings.</span></span> <span data-ttu-id="ab613-105">バックアップ ファイルからクリーンアップされたデータ要素の一覧を確認します。</span><span class="sxs-lookup"><span data-stu-id="ab613-105">Review the list of data elements that are cleaned up from the backup file.</span></span>
4. <span data-ttu-id="ab613-106">インポート操作をすぐに開始します。</span><span class="sxs-lookup"><span data-stu-id="ab613-106">The import operation will begin immediately.</span></span>


<span data-ttu-id="ab613-107">データベース バックアップ (.bacpac) ファイルをダウンロードした後、データベースを開発環境にインポートするには、レベル 1 環境の手動インポート操作の開始が可能です。</span><span class="sxs-lookup"><span data-stu-id="ab613-107">To import a database to a developer environment after you've downloaded a database backup (.bacpac) file, you can begin the manual import operation on your Tier 1 environment.</span></span> <span data-ttu-id="ab613-108">データベースをインポートするときは、これらのガイドラインに従うことお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ab613-108">When you import the database, we recommend that you follow these guidelines:</span></span>

- <span data-ttu-id="ab613-109">必要な場合は、後で戻すことができるように、既存の AxDB データベースのコピーを保持します。</span><span class="sxs-lookup"><span data-stu-id="ab613-109">Keep a copy of the existing AxDB database, so that you can revert to it later if needed.</span></span>
- <span data-ttu-id="ab613-110">**AxDB\_fromProd** などの新しい名前の下に新しいデータベースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="ab613-110">Import the new database under a new name, such as **AxDB\_fromProd**.</span></span>

<span data-ttu-id="ab613-111">最良のパフォーマンスを確実にするためには、\*.bacpac ファイルをインポート元のコンピューターにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ab613-111">To ensure the best performance, copy the \*.bacpac file to the local computer that you're importing from.</span></span> <span data-ttu-id="ab613-112">sqlpackage .NET Core for Windows を [Get sqlpackage .NET Core for Windows](https://docs.microsoft.com/sql/tools/sqlpackage-download?view=sql-server-ver15#get-sqlpackage-net-core-for-windows) からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="ab613-112">Download sqlpackage .NET Core for Windows from [Get sqlpackage .NET Core for Windows](https://docs.microsoft.com/sql/tools/sqlpackage-download?view=sql-server-ver15#get-sqlpackage-net-core-for-windows).</span></span> <span data-ttu-id="ab613-113">**コマンド プロンプト** ウィンドウを開き、sqlpackage .NET Core フォルダーから次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ab613-113">Open a **Command Prompt** window, and run the following commands from the sqlpackage .NET Core folder.</span></span>

```

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:localhost /tdn:<target database name> /p:CommandTimeout=1200
```

<span data-ttu-id="ab613-114">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="ab613-114">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="ab613-115">**tsn (ターゲット サーバー名)** – インポートする Microsoft SQL Server インスタンスの名前。</span><span class="sxs-lookup"><span data-stu-id="ab613-115">**tsn (target server name)** – The name of the Microsoft SQL Server instance to import into.</span></span>
- <span data-ttu-id="ab613-116">**tdn(ターゲット データベース名)** – インポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="ab613-116">**tdn (target database name)** – The name of the database to import into.</span></span> <span data-ttu-id="ab613-117">データベースが既に存在していては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="ab613-117">The database should **not** already exist.</span></span>
- <span data-ttu-id="ab613-118">**sf(ソース ファイル)** – インポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="ab613-118">**sf (source file)** – The path and name of the file to import from.</span></span>

> [!NOTE]
> <span data-ttu-id="ab613-119">インポート中に、ユーザー名およびパスワードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ab613-119">During import, the user name and password aren't required.</span></span> <span data-ttu-id="ab613-120">既定では、SQL Server は、現在サインインしているユーザーに対して Microsoft Windows 認証を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab613-120">By default, SQL Server uses Microsoft Windows authentication for the user who is currently signed in.</span></span>

<span data-ttu-id="ab613-121">レベル 1 の環境に手動インポート処理を実行する方法については、[データベースのインポート](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/database/dbmovement-scenario-exportuat#import-the-database) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab613-121">For information about how to complete the manual import operations into a Tier 1 environment, see [Import the database](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/database/dbmovement-scenario-exportuat#import-the-database).</span></span> 
