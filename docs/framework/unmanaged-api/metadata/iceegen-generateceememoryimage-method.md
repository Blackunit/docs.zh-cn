---
title: "ICeeGen::GenerateCeeMemoryImage 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICeeGen.GenerateCeeMemoryImage
api_location: mscoree.dll
api_type: COM
f1_keywords: ICeeGen::GenerateCeeMemoryImage
helpviewer_keywords:
- ICeeGen::GenerateCeeMemoryImage method [.NET Framework metadata]
- GenerateCeeMemoryImage method [.NET Framework metadata]
ms.assetid: b3847495-0ae6-4a72-b496-65ce2424afc6
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: d79d1e59994dbe13c2124646e943161392846fc3
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="iceegengenerateceememoryimage-method"></a><span data-ttu-id="28f40-102">ICeeGen::GenerateCeeMemoryImage 方法</span><span class="sxs-lookup"><span data-stu-id="28f40-102">ICeeGen::GenerateCeeMemoryImage Method</span></span>
<span data-ttu-id="28f40-103">在基本代码的内存中生成的映像。</span><span class="sxs-lookup"><span data-stu-id="28f40-103">Generates an image in memory for the code base.</span></span>  
  
 <span data-ttu-id="28f40-104">此方法已过时，不应使用。</span><span class="sxs-lookup"><span data-stu-id="28f40-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28f40-105">语法</span><span class="sxs-lookup"><span data-stu-id="28f40-105">Syntax</span></span>  
  
```  
HRESULT GenerateCeeMemoryImage (  
    [out] void    **ppImage  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="28f40-106">参数</span><span class="sxs-lookup"><span data-stu-id="28f40-106">Parameters</span></span>  
 `ppImage`  
 <span data-ttu-id="28f40-107">[out]指向所生成的图像的指针。</span><span class="sxs-lookup"><span data-stu-id="28f40-107">[out] A pointer to the generated image.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="28f40-108">要求</span><span class="sxs-lookup"><span data-stu-id="28f40-108">Requirements</span></span>  
 <span data-ttu-id="28f40-109">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="28f40-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="28f40-110">**标头：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="28f40-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="28f40-111">**库：**用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="28f40-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="28f40-112">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="28f40-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28f40-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="28f40-113">See Also</span></span>  
 [<span data-ttu-id="28f40-114">ICeeGen 接口</span><span class="sxs-lookup"><span data-stu-id="28f40-114">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)