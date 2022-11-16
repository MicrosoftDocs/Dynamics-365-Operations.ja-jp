---
title: 性別基準の列挙型の拡張性
description: この記事では、性別基準のリスト (列挙型) の拡張性の概要について説明します。
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749316"
---
# <a name="gender-base-enum-extensibility"></a>性別基準の列挙型の拡張性

**Gender** リスト (列挙型) が拡張できるようになりました。 この記事では、**Gender** 列挙型を拡張する予定がある場合、コード ベースで行う必要がある変更について説明します。

## <a name="gender-vs-hcmpersongender"></a>Gender と HcmPersonGender

性別の値には 2 つの列挙型があります:

- **Gender** (アプリケーション プラットフォーム)
- **HcmPersonGender** (PersonnelManagement)

**Gender** 列挙型は Microsoft Dynamics 365 Finance 全体で使用されますが、**HcmPersonGender** は人材管理 (HCM) 機能に固有のものです。 HCM 機能を使用し、**Gender** 列挙型に変更を加える場合は、**HcmPersonGender** についても同様の変更を検討する必要があります。 たとえば、**トランスジェンダー** を **Gender** 列挙に追加する場合は、**トランスジェンダー** を **HcmPersonGender** の列挙に追加します。

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (クラス)

新しい **HcmPersonGenderTranformUtil** クラスが作成され、2 つの基本列挙子間で変換が可能になりました。 このクラスでは、**convertGenderToHcmPersonGender** と **convertHcmPersonGenderToGender** の 2 つのメソッドがあります。 **Chain of Command** クラスまたは **イベント ハンドラー** を使用して拡張子を作成し、両方のメソッドを拡張して、どちらかの基本列挙型に追加される新しい値をマップする必要があります。

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (クラス)

**PayrollStateWageTaxPrepDP** は、**Payroll State Wage Tax Prep** SQL Server Reporting Services (SSRS) レポート用のデータ プロバイダー クラスです。 米国では 3 つの値を使用できます: **Male**、**Female**、**Unspecified**。 **populatePayrollStateWageTaxPrepTmp** メソッドには、**HcmPersonGender** 列挙型の値を 次の 3 つのフィールドのいずれかにマップするために使用される switch ステートメントがあります: **IsMale**、**IsFemale**、**IsUnspecifiedGender**。 switch ステートメントの既定値は **IsUnspecifiedGender** です。 **HcmPersonGender** 列挙型に値を追加して異なるマップを行う場合、必要に応じて、**populatePayrollStateWageTaxPrepTmp** メソッドで **Chain of Command** クラスを使用して拡張子を作成し、値を変更する必要があります。

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (クラス)

**smmOutlookSync_Contact** 統合クラスは、**Outlook** と **連絡担当者** との間で値 をリンクします。 **Outlook** では 3 つの値がサポートされています: **Male**、**Female**、**Unspecified**。 このクラスには、**Genders** を **OutlookGenders** にマップするのに役立つ 2 つのメソッドがあります。 既定のメソッドは **NonSpecific/UnSpecified** です。 **Gender** 列挙型に追加の値を作成する場合は、必要に応じて両方のメソッドとマップに対して **Chain of Command** クラスを使用して拡張子を作成する必要があります。
