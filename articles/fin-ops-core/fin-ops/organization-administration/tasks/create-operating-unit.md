---
title: 作業単位の作成
description: 作業単位とは、事業における経済資源と運営プロセスの管理を振り分ける際に使用する組織です。
author: sericks007
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMOperatingUnit, OMInternalOrganizationSelector
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc0020a7f7aa60305bfc7c66474e0bbc26f27bef
ms.sourcegitcommit: d38d2fe85dc2497211ba5731617f590029d07145
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809561"
---
# <a name="create-an-operating-unit"></a>作業単位の作成

[!include [banner](../../includes/banner.md)]

作業単位とは、事業における経済資源と運営プロセスの管理を振り分ける際に使用する組織です。 作業単位のメンバは、希少なリソースの有効活用、プロセスの改善、および業績に対する責任を担っています。 作業単位の種類には、コスト センター、事業単位、部門、およびバリュー ストリームが含まれます。 作業単位を作成するには、次の手順に従います。 この手順の作成に使用するデモ データの会社は USMF です。

1. **ナビゲーション ウィンドウ > モジュール > 組織管理 > 組織 > 作業単位** の順に移動します。
2. **新規** をクリックすると、ドロップ ダイアログが開きます。
3. 一覧で、目的のレコードを見つけ、選択します。 作成する作業単位のタイプを選択します。  
4. 一覧で、選択された行のリンクをクリックします。
5. **名前** フィールドに値を入力します。
    + 必要に応じて、**一般** セクションを展開します。  
    + ID 番号、DUNS 番号、およびマネージャーなど、作業単位に関する一般情報を入力します。    
    + 必要に応じて、**住所** セクションを展開します。  
    + 番地、郵便番号、市町村などの住所情報を入力します。 **追加** をクリックして新しい住所レコードを入力するか、編集をクリックして既存の住所レコードを変更します。   
    + 必要に応じて、**連絡先情報** セクションを展開します。  
    + 電子メール アドレス、URL と電話番号など通信方法に関する情報を入力します。 新しい通信記録を入力するには、[新規] をクリックします。 既存の通信記録を変更するには、**詳細オプション > 詳細** の順にクリックします。   
6. 必要に応じて **作業単位数** を変更します。 この番号は、対応する **関係者** レコードに固有の ID であり、その他の作業単位と同じではありません。
7. **保存** を選択します。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
