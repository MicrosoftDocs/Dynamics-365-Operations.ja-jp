---
title: "クラウドの POS と MPOS の拡張ログオン機能の設定"
description: "このトピックでは、クラウド POS と Retail Modern POS (MPOS) の拡張ログオンを設定するためのオプションについて説明します。"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e29aea4509dd323c295b02f289fbcfa46fab3392
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>クラウドの POS と MPOS の拡張ログオン機能の設定

[!include[banner](includes/banner.md)]


このトピックでは、クラウド POS と Retail Modern POS (MPOS) の拡張ログオンを設定するためのオプションについて説明します。

<a name="setting-up-extended-logon"></a>拡張ログオンの設定
=========================

バーコード マスクの設定は、[**小売**] &gt; [**チャンネル設定**] &gt; [**POS 設定**] &gt; [**POS プロファイル**] &gt; [**機能プロファイル**] にあります。 [**機能**] クイック タブには、拡張ログオンに関連付けられる次のオプションが含まれています。

### <a name="staff-bar-code-logon"></a>スタッフ バーコード ログオン

[**スタッフ バーコード ログオン**] オプションが有効な場合、POS 資格情報に割り当てられた拡張ログオンを持っている作業者は、バーコードを使用してログオンできます。

### <a name="staff-bar-code-logon-requires-password"></a>スタッフ バーコード ログオンにパスワードが必要

パスワードが必要となる [**スタッフ バーコード ログオン**] オプションが有効な場合は、スタッフ バーコード ログオンは表示された拡張ログオンに割り当てられている作業者のみが選択されます。 このオプションを有効にする場合、作業者はパスワードを入力する必要があります。

### <a name="staff-card-logon"></a>スタッフ カード ログオン

[**スタッフ カード ログオン**] オプションが有効な場合、POS 資格情報に割り当てられた拡張ログオンを持っている作業者は、磁気ストライプを使用してログオンできます。

### <a name="staff-card-logon-requires-password"></a>スタッフ カード ログオンにパスワードが必要

パスワードが必要となる [**スタッフ カード ログオン**] オプションが有効な場合は、スタッフ カード ログオンは表示された拡張ログオンに割り当てられている作業者のみが選択されます。 このオプションを有効にする場合、作業者はパスワードを入力する必要があります。

<a name="assigning-an-extended-logon"></a>拡張ログオンの割り当て
===========================

既定では、マネージャのみが作業者に拡張ログオンを割り当てることができます。 拡張ログオンを割り当てるには、POS で [**拡張ログオン**] に移動します。 検索フィールドに、オペレーター ID を入力して、作業者を検索します。 作業者を選択し、[**割り当て**] をクリックします。 次のページで、作業者に割り当てる拡張ログオンを機械に通すかスキャンします。 読み取りまたはスキャンが正常に読み取られた場合、[**OK**] ボタンが使用できるようになります。 その作業者の拡張ログオンを保存する場合、[**OK**] をクリックします。

<a name="deleting-an-extended-logon"></a>拡張ログオンの削除
==========================

作業者に割り当てられている拡張ログオンを削除するには、[**拡張ログオン**] 操作にて作業者を検索します。 作業者を選択し、[**割り当て解除**] をクリックします。 その作業者と関連付けられるすべての拡張ログオン資格情報が削除されます。

<a name="extending-extended-logon"></a>拡張ログオンの拡張
========================

ログオン サービスはパーム スキャナーなどの追加ログオン デバイスをサポートするために、拡張できます。 詳細については、POS 拡張ドキュメントを参照してください。

<a name="using-extended-logon"></a>拡張ログオンの使用
====================

拡張ログオンを構成すると、作業者にバーコードまたは磁気ストライプが割り当てられ、作業者は POS ログオン ページが表示されている間に、自分のカードを読み取るか、またはスキャンする必要があります。 ログオンを続行する前にパスワードが必要な場合、作業者は自分のパスワードを入力するように要求されます。




