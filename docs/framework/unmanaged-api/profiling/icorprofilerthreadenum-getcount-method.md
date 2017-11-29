---
title: "ICorProfilerThreadEnum::GetCount 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerThreadEnum.GetCount
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerThreadEnum::GetCount
helpviewer_keywords:
- ICorProfilerThreadEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerThreadEnum interface [.NET Framework profiling]
ms.assetid: d6dbdc4a-6115-455d-a3f3-704a81d3646b
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: ae6e5324328eef8d86e0202e30012ffaba45beab
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerthreadenumgetcount-method"></a><span data-ttu-id="564bf-102">ICorProfilerThreadEnum::GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="564bf-102">ICorProfilerThreadEnum::GetCount Method</span></span>
<span data-ttu-id="564bf-103">获取应用程序使用的线程数。</span><span class="sxs-lookup"><span data-stu-id="564bf-103">Gets the number of threads that are used by the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="564bf-104">语法</span><span class="sxs-lookup"><span data-stu-id="564bf-104">Syntax</span></span>  
  
```  
HRESULT GetCount (    [out] ULONG * pcelt  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="564bf-105">参数</span><span class="sxs-lookup"><span data-stu-id="564bf-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="564bf-106">[out]应用程序使用的线程数。</span><span class="sxs-lookup"><span data-stu-id="564bf-106">[out] The number of threads used by the application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="564bf-107">要求</span><span class="sxs-lookup"><span data-stu-id="564bf-107">Requirements</span></span>  
 <span data-ttu-id="564bf-108">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="564bf-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="564bf-109">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="564bf-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="564bf-110">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="564bf-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="564bf-111">**.NET framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="564bf-111">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="564bf-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="564bf-112">See Also</span></span>  
 [<span data-ttu-id="564bf-113">ICorProfilerThreadEnum 接口</span><span class="sxs-lookup"><span data-stu-id="564bf-113">ICorProfilerThreadEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md)  
 [<span data-ttu-id="564bf-114">分析接口</span><span class="sxs-lookup"><span data-stu-id="564bf-114">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)