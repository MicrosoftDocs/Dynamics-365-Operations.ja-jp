---
title: 確認後支払の概要
description: この記事は確認後支払についての情報を提供し、銀行に提出する小切手の電子リストを生成するのに使用されます。
author: panolte
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: ffb2ded8c6f1e86657f298f3638da39ac4c63b66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972109"
---
# <a name="positive-pay-overview"></a>確認後支払の概要

[!include [banner](../includes/banner.md)]

この記事は確認後支払についての情報を提供し、銀行に提出する小切手の電子リストを生成するのに使用されます。 

確認後支払を使用し、銀行に渡す小切手の電子リストを生成します。 確認後支払ファイルは、銀行が小切手の不正を禁止するのに役立ちます。 小切手が印刷されるたびに、小切手の電子リストを生成するための確認後支払を設定します。 小切手が銀行に提出されるとき、銀行はその小切手を事前に提出された小切手のリストと比較します。 小切手がリストの小切手と一致する場合、銀行は小切手を決済します。 小切手がリスト内の小切手と一致しない場合、銀行は確認のために小切手を保留にします。

確認後支払は SafePay とも呼ばれます。 

確認後支払ファイルには、受取人と小切手金額に関する機密情報が含まれている場合があります。 したがって、ファイルを生成時から銀行がそのファイルを受領するまで、適切なセキュリティ対策をかならず使用します。 確認後支払ファイルは、Web ブラウザのダウンロードの手順に従ってダウンロードされます。 

確認後支払ファイルは、データ エンティティを使用して作成されます。 確認後支払ファイルを生成する前に、銀行が実行できる形式にデータを変換する XML の変換形式を設定する必要があります。 

確認後支払情報を生成する銀行口座ごとに、確認後支払形式を割り当てる必要があります。 確認後支払ファイルを生成した後に、一つの法人と一つの銀行口座に対する確認後支払ファイルを生成できます。 また、複数の法人と銀行口座の確認後支払ファイルを同時に生成することもできます。 

確認後支払ファイルに記載されている小切手が支払われた後、銀行から確認番号を受け取ります。 その後、システムで確認後支払ファイルを確認できます。 

確認後支払ファイルを変更する必要がある場合は、それを取り消すことができます。 その後、確認後支払ファイルの小切手ごとに、小切手が確認後支払ファイルに含まれているかどうかを示すフィールドがリセットされます。

詳細については、「[確認後支払ファイルの設定と生成](set-up-generate-positive-pay-files.md)」を参照してください。



