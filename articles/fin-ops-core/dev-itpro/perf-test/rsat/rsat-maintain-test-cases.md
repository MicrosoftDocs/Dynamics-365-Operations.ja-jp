---
title: Regression Suite Automation Tool (RSAT) でのテスト ケースの管理
description: このトピックでは、Regression suite automation tool (RSAT) でテスト ケースと添付ファイルを管理する方法について説明します。
author: FrankDahl
ms.date: 04/12/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2021-04-12
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccfd1e3e55c70fc70af8cc595ef48008600a1c2a
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936042"
---
# <a name="maintain-test-cases-in-regression-suite-automation-tool-rsat"></a><span data-ttu-id="6e7d1-103">Regression Suite Automation Tool (RSAT) でのテスト ケースの管理</span><span class="sxs-lookup"><span data-stu-id="6e7d1-103">Maintain test cases in Regression suite automation tool (RSAT)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6e7d1-104">Regression suite automation tool (RSAT) のバージョン 2.2 以降を使用すると、ツール自体でテスト ケースと添付ファイルを管理できます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-104">Regression suite automation tool (RSAT) version 2.2 and later lets you maintain test cases and attachments in the tool itself.</span></span> <span data-ttu-id="6e7d1-105">以前のバージョンでは、テスト ケースを管理するために Microsoft Azure DevOps を使用し、テストを実行するために RSAT に切り替えなければなりませんでした。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-105">In earlier versions, you had to use Microsoft Azure DevOps to maintain test cases and then switch to RSAT to run tests.</span></span> <span data-ttu-id="6e7d1-106">したがって、新しいバージョンは操作性がより向上し、生産性の向上に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-106">Therefore, newer versions offer better usability and help improve productivity.</span></span> <span data-ttu-id="6e7d1-107">多くの操作を RSAT で完全に行うことができ、テスト スイートでの作業も容易です。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-107">Many operations can be done completely in RSAT, and it's also easier to work with test suites.</span></span>

<span data-ttu-id="6e7d1-108">テスト計画およびテスト スイートは Azure DevOps で引き続き管理されています。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-108">Test plans and test suites continue to be maintained in Azure DevOps.</span></span>

<span data-ttu-id="6e7d1-109">この機能を使用するには、**Azure DevOps へのアップロードを有効にする** オプションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-109">To use this feature, you must enable the **Enable upload to Azure DevOps** option.</span></span> <span data-ttu-id="6e7d1-110">RSAT で加えられた変更はその後 Azure DevOps に自動的にアップロードされ、そこで使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-110">Changes that are made in RSAT are then automatically uploaded to Azure DevOps and will be available there.</span></span> <span data-ttu-id="6e7d1-111">したがって、テスト スイートには、 他のユーザーが使用可能な、またはパイプラインを使用して Azure DevOps で実行できるアップデートされたテスト ケースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-111">Therefore, test suites will include the updated test cases that are available to other users or that can be run in Azure DevOps by a pipeline.</span></span>

## <a name="view-test-case-information"></a><span data-ttu-id="6e7d1-112">テスト ケース情報の表示</span><span class="sxs-lookup"><span data-stu-id="6e7d1-112">View test case information</span></span>

<span data-ttu-id="6e7d1-113">テスト ケース情報を表示するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-113">Follow these steps to view information about a test case.</span></span>

1. <span data-ttu-id="6e7d1-114">**テスト ケース** グリッドで、関連するテスト ケースを検索し、省略記号ボタン (**...**) が **タイトル** 列と **パラメーター ファイル** 列の間で表示されるまで行をポイントします。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-114">In the **Test Cases** grid, find the relevant test case, and hover over the row until an ellipsis button (**...**) appears between the **Title** and **Parameters File** columns.</span></span>

    ![テスト ケース グリッドの省略記号ボタン](media/test-case-details.PNG)

2. <span data-ttu-id="6e7d1-116">省略記号ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-116">Select the ellipsis button.</span></span> <span data-ttu-id="6e7d1-117">表示されるメニューには、**テスト ケースを開く** および **テストケースを削除する** という 2 つのコマンドがあります。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-117">The menu that appears has two commands: **Open test case** and **Delete Test Case**.</span></span>

    ![省略記号ボタン メニューのコマンド](media/test-case-details-context.PNG)

3. <span data-ttu-id="6e7d1-119">**テスト ケースを開く** を選択すると、**テスト ケース情報** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-119">Select **Open test case** to open the **Test Case information** dialog box.</span></span>

    ![テスト ケース情報ダイアログ ボックス](media/test-case-information.PNG)

<span data-ttu-id="6e7d1-121">**テスト ケース情報** ダイアログ ボックスに、テスト ケースに関する以下の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-121">The **Test Case information** dialog box shows the following information about the test case:</span></span>

+ <span data-ttu-id="6e7d1-122">ダイアログ ボックスの上部にテスト スイートのテスト ケースに割り当てられている名前が表示されており、変更できます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-122">The name that is assigned to the test case in the test suite appears at the top of the dialog box and can be changed.</span></span>
+ <span data-ttu-id="6e7d1-123">記録の名前は、テスト ケース名の下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-123">The recording name appears under the test case name.</span></span> <span data-ttu-id="6e7d1-124">この名前は、 Finance and Operations アプリのタスク レコーダーで、または販売時点管理 (POS) クライアントを使用して記録された場合に使用された記録 XML ファイルから取得されます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-124">This name is taken from the recording XML file that was used when the recording was made in Task Recorder in the Finance and Operations app or by using the point of sale (POS) client.</span></span>
+ <span data-ttu-id="6e7d1-125">**添付ファイル** グリッドには、テスト ケースで使用できる添付ファイルの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-125">The **Attachments** grid shows the list of attachment files that are available with the test case.</span></span> <span data-ttu-id="6e7d1-126">この一覧は、添付ファイルのサブフォルダーの下の **ディレクトリ** アクションを使用して検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-126">You can also find this list by using the **Directory** action under the attachments subfolder.</span></span>

## <a name="create-a-test-case-that-has-attachments"></a><span data-ttu-id="6e7d1-127">添付ファイルがあるテスト ケースの作成</span><span class="sxs-lookup"><span data-stu-id="6e7d1-127">Create a test case that has attachments</span></span>

<span data-ttu-id="6e7d1-128">次の手順に従って、RSAT を使用して新しいテスト ケースを追加します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-128">Follow these steps to add a new test case by using RSAT.</span></span>

1. <span data-ttu-id="6e7d1-129">(この例では、**仕入から支払 – v2**) に新しいテスト ケースを追加するテスト スイートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-129">Select the test suite that you want to add a new test case to (**Procure to Pay – v2** in this example).</span></span> <span data-ttu-id="6e7d1-130">その後 **テスト ケース** を選択して開くと、**テスト ケース情報** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-130">Then select **New Test Case** to open the **Test Case information** dialog box.</span></span>

    ![新しいテスト ケース ボタン](media/test-case-add.PNG)

2. <span data-ttu-id="6e7d1-132">テスト ケースの名前を入力し、添付ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-132">Enter the name of the test case, and add attachment files.</span></span> <span data-ttu-id="6e7d1-133">これらのファイルには、テスト ケースの手順を含む記録 XML ファイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-133">These files include the recording XML file that contains steps for the test case.</span></span> <span data-ttu-id="6e7d1-134">添付ファイルを追加するには、**追加** を選択し、ダイアログ ボックスでそのファイルが表示され、そのファイルを選択して添付ファイルとして追加します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-134">To add attachment files, select **Add**, and then, in the dialog box that appears, select the files to add as attachments.</span></span>
3. <span data-ttu-id="6e7d1-135">完了したら、**保存** を選択して新しいテスト ケースを保存するか、または **キャンセル** を選択してそれを破棄します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-135">When you've finished, select **Save** to save the new test case or **Cancel** to discard it.</span></span>

    ![追加ボタンと保存ボタン](media/add-test-case.PNG)

<span data-ttu-id="6e7d1-137">新しいテスト ケースを保存する場合、選択した添付ファイルが、RSAT によってローカルの RSAT 作業ディレクトリにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-137">When you save a new test case, RSAT copies the attachment files that you selected into your local RSAT working directory.</span></span> <span data-ttu-id="6e7d1-138">コピーは、テスト ケースで使用できるような方法で保持されます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-138">It maintains the copies there so that they can be used with the test case.</span></span>

<span data-ttu-id="6e7d1-139">1 つのテスト セットから別のテスト セットにテスト ケースを自動的に複製する機能はありません。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-139">There is no feature that automatically clones test cases from one test suite to another.</span></span> <span data-ttu-id="6e7d1-140">ただし、次の手順に従って手動でテスト ケースを複製することができます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-140">However, but you can manually clone test cases by following these steps.</span></span>

1. <span data-ttu-id="6e7d1-141">前の手順の記載に従ってテスト ケースを作成します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-141">Create a test case as described in the previous procedure.</span></span> <span data-ttu-id="6e7d1-142">この手順の一部として、記録 XML ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-142">As part of this step, add the recording XML file.</span></span>
2. <span data-ttu-id="6e7d1-143">新しいテスト ケースを保存し、それに割り当てられている **CaseID** 値を記録します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-143">Save the new test case, and make a note of the **CaseID** value that is assigned to it.</span></span>
3. <span data-ttu-id="6e7d1-144">パラメーター Excel ファイルを新しいテスト ケースに追加できます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-144">You can add a parameter Excel file to the new test case.</span></span> <span data-ttu-id="6e7d1-145">ただし、ファイル名は新しい **CaseID** 値と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-145">However, the file name must match the new **CaseID** value.</span></span> <span data-ttu-id="6e7d1-146">複製するテスト ケースからパラメーター Excel ファイルをコピーし、**CaseID** 値に一致するようにコピーのファイル名を変更します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-146">Copy the parameter Excel file from the test case that you're cloning, and change the file name of the copy so that it matches the new **CaseID** value.</span></span>
4. <span data-ttu-id="6e7d1-147">新しいパラメーター Excel ファイルを開き、すべての古い **CaseID** 値のインスタンスを新しい **CaseID** 値に変更します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-147">Open the new parameter Excel file, and change all instances of the old **CaseID** value to the new **CaseID** value.</span></span>
5. <span data-ttu-id="6e7d1-148">新しいパラメーター Excel ファイルの更新を完了したら、新しいテスト ケースに添付ファイルとして追加します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-148">After you've finished updating the new parameter Excel file, add it to the new test case as an attachment.</span></span>

<span data-ttu-id="6e7d1-149">または、最初に新しいテスト ケース用のパラメーター Excel ファイルを生成してから、そのファイルを、複製するテスト ケースのパラメーター Excel ファイルと一致するように手動で編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-149">Alternatively, you can generate a parameter Excel file for the new test case first, and then manually edit it so that it matches the parameter Excel file of the test case that you're cloning.</span></span>

## <a name="remove-an-attachment-from-a-test-case"></a><span data-ttu-id="6e7d1-150">テスト ケースからの添付ファイルの削除</span><span class="sxs-lookup"><span data-stu-id="6e7d1-150">Remove an attachment from a test case</span></span>

<span data-ttu-id="6e7d1-151">必要ではなくなったときに、添付ファイルをテスト ケースから削除できます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-151">You can remove attachments from a test case when you no longer require them.</span></span>

- <span data-ttu-id="6e7d1-152">**テスト ケース情報** ダイアログ ボックスで、添付ファイル用の行を選択したまま (または右クリック) にして、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-152">In the **Test Case information** dialog box, select and hold (or right-click) the row for the attachment file, and then select **Remove**.</span></span>

    ![削除ボタン](media/remove-attachment.PNG)

<span data-ttu-id="6e7d1-154">記録 XML ファイルを編集し、新しいバージョンをテスト ケースにアップロードする場合も、この手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-154">You can also use this procedure if you've edited the recording XML file and you want to upload the new version to the test case.</span></span> <span data-ttu-id="6e7d1-155">この場合、まず既存のファイルを削除してから、新しいファイルを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-155">In this case, you should first remove the existing file and then add the new file.</span></span>

## <a name="delete-a-test-case"></a><span data-ttu-id="6e7d1-156">テスト ケースの削除</span><span class="sxs-lookup"><span data-stu-id="6e7d1-156">Delete a test case</span></span>

<span data-ttu-id="6e7d1-157">次の手順に従ってテスト ケースを削除します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-157">Follow these steps to delete a test case.</span></span>

1. <span data-ttu-id="6e7d1-158">**テスト ケース** グリッドで、関連するテスト ケースを検索し、省略記号ボタン (**...**) が **タイトル** 列と **パラメーター ファイル** 列の間で表示されるまで行をポイントします。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-158">In the **Test Cases** grid, find the relevant test case, and hover over the row until an ellipsis button (**...**) appears between the **Title** and **Parameters File** columns.</span></span>
2. <span data-ttu-id="6e7d1-159">省略記号ボタンを選択し、メニューの **テスト ケースの削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-159">Select the ellipsis button, and then select **Delete Test Case** on the menu.</span></span>

    ![テスト ケースの削除のコマンド](media/delete-test-case.PNG)

3. <span data-ttu-id="6e7d1-161">テスト ケースを削除することを確認し、必要に応じて削除の理由を指定します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-161">Confirm that you want to delete the test case, and optionally specify a reason for the deletion.</span></span>

<span data-ttu-id="6e7d1-162">RSAT で削除するテスト ケースは、 ローカルと Azure DevOps の現在のテスト スイートから削除されます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-162">A test case that you delete in RSAT is removed from the current test suite, both locally and in Azure DevOps.</span></span>

<span data-ttu-id="6e7d1-163">Azure DevOps では作業項目はテスト ケースを表し、テスト スイートにはテスト ケースの作業項目へのリンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-163">In Azure DevOps, work items represent test cases, and test suites contain links to the test case work items.</span></span> <span data-ttu-id="6e7d1-164">テスト ケースは、複数のテスト スイートからテスト ケースにリンクして再利用されます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-164">A test case is reused by linking to it from more than one test suite.</span></span> <span data-ttu-id="6e7d1-165">RSAT でテスト ケースを削除すると、RSAT はテスト ケースが 1 つのテスト スイートにリンクするか、複数のテスト スイートにリンクするかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-165">When a test case is deleted in RSAT, RSAT determines whether the test case is linked to one test suite or more than one test suite.</span></span> <span data-ttu-id="6e7d1-166">テスト ケースが現在のテスト スイートのみで使用されている場合は、RSAT によってテスト ケースを表す Azure DevOps 作業項目が削除されます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-166">If the test case is used only by the current test suite, RSAT deletes the Azure DevOps work item that represents the test case.</span></span> <span data-ttu-id="6e7d1-167">テスト ケースが他のテスト スイートで使用されている場合、RSAT によってこの作業項目自体は削除されません。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-167">If the test case is used by other test suites, RSAT doesn't delete the work item itself.</span></span> <span data-ttu-id="6e7d1-168">代わりに、作業項目へのリンクだけが削除されます。</span><span class="sxs-lookup"><span data-stu-id="6e7d1-168">Instead, it deletes only the link to the work item.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
