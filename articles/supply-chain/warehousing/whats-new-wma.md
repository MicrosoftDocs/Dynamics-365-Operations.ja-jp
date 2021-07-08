---
title: Warehouse Management モバイル アプリの新機能または変更された機能
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の Warehouse Management モバイル アプリのリリース済バージョンごとに、新機能および変更された機能を一覧表示します。
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261786"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="ec97f-103">Warehouse Management モバイル アプリの新機能または変更された機能</span><span class="sxs-lookup"><span data-stu-id="ec97f-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec97f-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management の Warehouse Management モバイル アプリのリリース済バージョンごとに、新機能、修正、改良点、および既知の問題を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="ec97f-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="ec97f-105">バージョン 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="ec97f-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="ec97f-106">バージョン 2.0.6.0 の管理の新機能、修正、および改良点</span><span class="sxs-lookup"><span data-stu-id="ec97f-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="ec97f-107">このバージョンでは、次の新機能、修正、および改良点を紹介します:</span><span class="sxs-lookup"><span data-stu-id="ec97f-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="ec97f-108">デモ モードでは、デバイス言語のすべてのラベルが表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="ec97f-109">次のエラー メッセージが表示される可能性は低くなります: "指定したサイズでは適切なビューが見つかりません。"</span><span class="sxs-lookup"><span data-stu-id="ec97f-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="ec97f-110">作業カードの最小高さが増加しました (作業一覧に表示されるフィールドが 3 つ以下になるよう構成されている場合)。</span><span class="sxs-lookup"><span data-stu-id="ec97f-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="ec97f-111">詳細カードの下部にあるマージン (フェードアウト) が改良されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="ec97f-112">サーバーと交換された XML ファイルの無効な記号が、適切に処理されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="ec97f-113">(たとえば、印刷不可能な文字が適切に処理され、アプリが応答を停止することはなくなりました。)</span><span class="sxs-lookup"><span data-stu-id="ec97f-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="ec97f-114">サーバー要求の送信時の HTTP エラー ("エラー 503" など) が、適切に処理されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="ec97f-115">エラーの表示中に、コンボ ボックス コントロールに対するオプションの一覧が自動的に表示されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="ec97f-116">ユーザー設定で選択された表示方向が原因で、アプリが応答を停止しなくなりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="ec97f-117">製品画像がセルフサービス環境に表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="ec97f-118">(この変更は、低解像度バージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="ec97f-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="ec97f-119">ファイル管理サービスでは、セルフサービス環境のフルサイズ画像はサポートされません。)</span><span class="sxs-lookup"><span data-stu-id="ec97f-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="ec97f-120">数量ゼロ ショート ピックが関係する問題は修正されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="ec97f-121">詳細カードに同一フィールドが複数表示される場合、アプリが応答を停止しなくなりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="ec97f-122">バージョン 2.0.6.0 の既知の問題</span><span class="sxs-lookup"><span data-stu-id="ec97f-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="ec97f-123">このバージョンには次の既知の問題があります:</span><span class="sxs-lookup"><span data-stu-id="ec97f-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="ec97f-124">アプリ (特に作業一覧) は時間の経過とともに遅くなります。</span><span class="sxs-lookup"><span data-stu-id="ec97f-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="ec97f-125">**Windows バージョン:** Window のスキャンに対して USB ガンを使用すると、結果の不整合により、スキャンした記号が混在します。</span><span class="sxs-lookup"><span data-stu-id="ec97f-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="ec97f-126">バージョン 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="ec97f-126">Version 2.0.5.0</span></span>

<span data-ttu-id="ec97f-127">このバージョンでは、次の新機能、修正、および改良点を紹介します:</span><span class="sxs-lookup"><span data-stu-id="ec97f-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="ec97f-128">クライアント シークレットは接続設定のセットアップで非表示になりません。</span><span class="sxs-lookup"><span data-stu-id="ec97f-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="ec97f-129">任意のテキストを長押しすると、完全に表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="ec97f-130">ストレージのアクセス許可がない場合のエラー メッセージが改善されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="ec97f-131">一部のフローに対して新しい制御順序が追加されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="ec97f-132">ウィンドウ サイズが原因で、送信ボタンを正しく使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="ec97f-133">大きなボタン サイズを使用する場合、小さい画面でスライダーを続行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="ec97f-134">4 ボタンのオーバーレイは、切り離されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="ec97f-135">キーボードが削除ボタンをサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="ec97f-136">キーボードを押す際に発生する明度問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="ec97f-137">デモ データに関するさまざまな問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="ec97f-138">詳細ページの数値フィールドに影響を与えた問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="ec97f-139">一部のデバイスで、画面キーボードが非表示になることがある問題が解決されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="ec97f-140">背景色や位置に影響を与えたバグなどの、ユーザー インターフェイス (UI) バグが修正されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="ec97f-141">ロシア語の UI が改良されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="ec97f-142">システムが応答を停止する原因となったさまざまな問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="ec97f-143">電卓の再開に関連した問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="ec97f-144">**Android バージョン:** Android 4.4 が起動時に応答を停止する原因となった問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="ec97f-145">**Android バージョン:** 最小スケーリングが 50% に減らされました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="ec97f-146">バージョン 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="ec97f-146">Version 2.0.4.0</span></span>

<span data-ttu-id="ec97f-147">バージョン 2.0.4.0 は Warehouse Management モバイル アプリの最初の一般公開リリースでした。</span><span class="sxs-lookup"><span data-stu-id="ec97f-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="ec97f-148">バージョン 2.0.4.0 の管理の新機能、修正、および改良点</span><span class="sxs-lookup"><span data-stu-id="ec97f-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="ec97f-149">このバージョンでは、プレビュー バージョンにはなかった次の新しい機能、修正、および改良点が導入されています。</span><span class="sxs-lookup"><span data-stu-id="ec97f-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="ec97f-150">詳細カードに同じデータを持つ 2 つのラベルが含まれる場合、ラベルの 1 つは非表示になります。</span><span class="sxs-lookup"><span data-stu-id="ec97f-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="ec97f-151">既定で特殊文字が表示され、非表示にするオプションがユーザー設定から削除されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="ec97f-152">無効な送信ボタンは、コンパクトなアーム持ちビューでは使用不可として表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="ec97f-153">コントロールの優先順位ロジックを変更すると、デバイス全体でのスケーリングが円滑になります。</span><span class="sxs-lookup"><span data-stu-id="ec97f-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="ec97f-154">したがって、フォントまたはボタンのスケーリング調整をする必要は少なくなります。</span><span class="sxs-lookup"><span data-stu-id="ec97f-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="ec97f-155">既定の色テーマが *濃い* に変更されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="ec97f-156">無効な送信ボタンの欠落しているアイコンが、リボン ビューに追加されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="ec97f-157">タイム アウト例外により、インライン エラーが表示される代わりに、接続ページに移動するようになります。</span><span class="sxs-lookup"><span data-stu-id="ec97f-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="ec97f-158">使用可能な送信アクションがない場合 (**OK**、**はい**、**承認**、**完了**、**完了済** など)、送信ボタンは無効になります。</span><span class="sxs-lookup"><span data-stu-id="ec97f-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="ec97f-159">アプリの安定性が改善されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-159">App stability has been improved.</span></span>
- <span data-ttu-id="ec97f-160">セキュリティの脆弱性 [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701) の修正プログラムがあります。</span><span class="sxs-lookup"><span data-stu-id="ec97f-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="ec97f-161">**Windows バージョン:** ウィンドウのサイズ変更後、メニューが応答しなくなる Windows の問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="ec97f-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="ec97f-162">バージョン 2.0.4.0 の既知の問題</span><span class="sxs-lookup"><span data-stu-id="ec97f-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="ec97f-163">このバージョンには次の既知の問題があります:</span><span class="sxs-lookup"><span data-stu-id="ec97f-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="ec97f-164">このバージョンには、Android 4.4 を使用するデバイスに問題があります。</span><span class="sxs-lookup"><span data-stu-id="ec97f-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="ec97f-165">この Android バージョンでアプリを使用すると、問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec97f-165">You might experience issues when you use the app on this Android version.</span></span>
