## <a name="mapping-tables"></a><span data-ttu-id="d6a8d-101">テーブルのマッピング</span><span class="sxs-lookup"><span data-stu-id="d6a8d-101">Mapping tables</span></span>

### <a name="mapping-types"></a><span data-ttu-id="d6a8d-102">マッピング タイプ</span><span class="sxs-lookup"><span data-stu-id="d6a8d-102">Mapping types</span></span>

<span data-ttu-id="d6a8d-103">さまざまな異なるマッピング タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="d6a8d-103">There are several different mapping types.</span></span> <span data-ttu-id="d6a8d-104">次の表は、テンプレート テーブルで使用される記号について説明します。</span><span class="sxs-lookup"><span data-stu-id="d6a8d-104">The following table explains the symbols used in the template tables.</span></span>

| <span data-ttu-id="d6a8d-105">記号</span><span class="sxs-lookup"><span data-stu-id="d6a8d-105">Symbol</span></span> | <span data-ttu-id="d6a8d-106">説明</span><span class="sxs-lookup"><span data-stu-id="d6a8d-106">Description</span></span> |
|--------|-------------|
| >  | <span data-ttu-id="d6a8d-107">一方向</span><span class="sxs-lookup"><span data-stu-id="d6a8d-107">One-way</span></span> |
| >> | <span data-ttu-id="d6a8d-108">一方向、データはプロセス内で変換されます。</span><span class="sxs-lookup"><span data-stu-id="d6a8d-108">One-way, and data is transformed in the process.</span></span> |
| =  | <span data-ttu-id="d6a8d-109">双方向</span><span class="sxs-lookup"><span data-stu-id="d6a8d-109">Bidirectional</span></span> |
| >< | <span data-ttu-id="d6a8d-110">双方向、データはプロセス内で変換されます。</span><span class="sxs-lookup"><span data-stu-id="d6a8d-110">Bidirectional, and data is transformed in the process.</span></span> |
| << | <span data-ttu-id="d6a8d-111">一方向、データはプロセス内で変換されます。</span><span class="sxs-lookup"><span data-stu-id="d6a8d-111">One-way, and data is transformed in the process.</span></span> |

### <a name="filters"></a><span data-ttu-id="d6a8d-112">フィルター</span><span class="sxs-lookup"><span data-stu-id="d6a8d-112">Filters</span></span>

<span data-ttu-id="d6a8d-113">ソースフィルタとリバースソースフィルタによって、どの行が同期されるかが決まります。</span><span class="sxs-lookup"><span data-stu-id="d6a8d-113">The source filter and reverse source filter determine which rows are synchronized.</span></span>

### <a name="default-values"></a><span data-ttu-id="d6a8d-114">既定値</span><span class="sxs-lookup"><span data-stu-id="d6a8d-114">Default values</span></span>

<span data-ttu-id="d6a8d-115">Finance and Operations テーブルまたは Customer Engagement テーブルのいずれにも同期フィールドが存在しない場合は、同期テーブルに既定値が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d6a8d-115">If a synchronized field does not exist in either the Finance and Operations table or the Customer Engagement table, then a default value is assigned in the synchronized table.</span></span> <span data-ttu-id="d6a8d-116">場合によっては、デフォルト値は、共通データモデル内の属性値へのルックアップである整数となります。</span><span class="sxs-lookup"><span data-stu-id="d6a8d-116">In some cases, the default value is an integer that is a lookup to an attribute value in the Common Data Model.</span></span> <span data-ttu-id="d6a8d-117">たとえば、共通データモデル の 取引先担当者 テーブルでは、 [**address1_addresstypecode**](../data-entities/dual-write-customer.md#customers-v3-to-contacts) の既定値は **3** です。</span><span class="sxs-lookup"><span data-stu-id="d6a8d-117">For example, in the Contacts table of the Common Data Model, the default value of [**address1_addresstypecode**](../data-entities/dual-write-customer.md#customers-v3-to-contacts) is **3**.</span></span> <span data-ttu-id="d6a8d-118">共通データモデルでは、 [address1AddressTypeCode](https://docs.microsoft.com/en-us/common-data-model/schema/core/applicationcommon/foundationcommon/contact#address1AddressTypeCode) に対する **3** の値は **プライマリー アドレス** です。</span><span class="sxs-lookup"><span data-stu-id="d6a8d-118">In the Common Data Model, for [address1AddressTypeCode](https://docs.microsoft.com/en-us/common-data-model/schema/core/applicationcommon/foundationcommon/contact#address1AddressTypeCode) the value of **3** is **Primary address**.</span></span> 
