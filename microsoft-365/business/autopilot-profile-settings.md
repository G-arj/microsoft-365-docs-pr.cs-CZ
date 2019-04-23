---
title: Informace o nastavení profilu AutoPilota .
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: conceptual
f1_keywords:
- ZTDProfileSettings
- O365E_ZTDProfileSettings
- BCS365_ZTDProfileSettings
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 99bfbf81-e719-4630-9b0f-c187edfa1f8a
description: AutoPilot profily umožňují určit, jak získá uživatel zařízení nainstalován systém Windows. Profily obsahují výchozí a volitelné nastavení, například Přeskočit instalaci Cortana.
ms.openlocfilehash: d43a15e5f3dc83596b5c23dd0ceb416b24810298
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2019
ms.locfileid: "32276935"
---
# <a name="about-autopilot-profile-settings"></a><span data-ttu-id="fba17-104">Informace o nastavení profilu AutoPilota .</span><span class="sxs-lookup"><span data-stu-id="fba17-104">About AutoPilot Profile settings</span></span>

## <a name="autopilot-profile-settings"></a><span data-ttu-id="fba17-105">Nastavení profilu autoPilot</span><span class="sxs-lookup"><span data-stu-id="fba17-105">AutoPilot profile settings</span></span>

<span data-ttu-id="fba17-106">Můžete určit, jak získá systém Windows nainstalován na zařízení uživatele pomocí profilů AutoPilot.</span><span class="sxs-lookup"><span data-stu-id="fba17-106">You can control how Windows gets installed on user devices by using the AutoPilot profiles.</span></span> <span data-ttu-id="fba17-107">Profily obsahují následující nastavení.</span><span class="sxs-lookup"><span data-stu-id="fba17-107">The profiles contain the following settings.</span></span>
  
 <span data-ttu-id="fba17-108">**AutoPilot výchozí funkce (povinné), které jsou automaticky nastaveny:**</span><span class="sxs-lookup"><span data-stu-id="fba17-108">**AutoPilot default features (required) that are set automatically:**</span></span>
  
|<span data-ttu-id="fba17-109">**Nastavení**</span><span class="sxs-lookup"><span data-stu-id="fba17-109">**Setting**</span></span>|<span data-ttu-id="fba17-110">**Popis**</span><span class="sxs-lookup"><span data-stu-id="fba17-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fba17-111">Vynechají registraci Cortana, OneDrive a OEM</span><span class="sxs-lookup"><span data-stu-id="fba17-111">Skip Cortana, OneDrive and OEM registration</span></span>  <br/> |<span data-ttu-id="fba17-112">Přeskočí instalace aplikace spotřebitele jako Cortana a osobní OneDrive.</span><span class="sxs-lookup"><span data-stu-id="fba17-112">Skips the installation of consumer apps like Cortana and personal OneDrive.</span></span> <span data-ttu-id="fba17-113">Tak dlouho, dokud je místní správce zařízení, můžete nainstalovat tyto novější zařízení uživatele.</span><span class="sxs-lookup"><span data-stu-id="fba17-113">The device user can install these later as long as he or she is a local admin on the device.</span></span> <span data-ttu-id="fba17-114">Původní registrace výrobce je vynechán, protože zařízení bude spravovat Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="fba17-114">The original manufacturer registration is skipped because the device will be managed by Microsoft 365 Business.</span></span>  <br/> |
|<span data-ttu-id="fba17-115">Přihlaste se zkušeností s vaší obchodní značky společnosti</span><span class="sxs-lookup"><span data-stu-id="fba17-115">Sign in experience with your company brand</span></span>  <br/> |<span data-ttu-id="fba17-116">Pokud má vaše společnost [Přidat vaše společnost vlastní Office 365 přihlašovací stránku](https://support.office.com/article/a1229cdb-ce19-4da5-90c7-2b9b146aef0a), dostane zařízení uživatele těchto zkušeností při přihlášení.</span><span class="sxs-lookup"><span data-stu-id="fba17-116">If your company has a [Add your company branding to Office 365 Sign In page](https://support.office.com/article/a1229cdb-ce19-4da5-90c7-2b9b146aef0a), the device user will get that experience when signing in.</span></span>  <br/> |
|<span data-ttu-id="fba17-117">MDM automatického zápisu s účty nakonfigurované zvukové poplašné zařízení.</span><span class="sxs-lookup"><span data-stu-id="fba17-117">MDM auto-enrollment with configured AAD accounts.</span></span>  <br/> |<span data-ttu-id="fba17-118">Identita uživatele budou spravovány službou Azure Active directory a uživatelé přihlášení do systému Windows a sady Office 365 pomocí svých pověření Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="fba17-118">The user identity will be managed by Azure Active directory, and the users will sign into Windows and Office 365 with their Microsoft 365 Business credentials.</span></span>  <br/> |
   
 <span data-ttu-id="fba17-119">**Volitelné nastavení:**</span><span class="sxs-lookup"><span data-stu-id="fba17-119">**Optional settings:**</span></span>
  
|<span data-ttu-id="fba17-120">**Nastavení**</span><span class="sxs-lookup"><span data-stu-id="fba17-120">**Setting**</span></span>|<span data-ttu-id="fba17-121">**Popis**</span><span class="sxs-lookup"><span data-stu-id="fba17-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fba17-122">Přeskočit nastavení ochrany osobních údajů (ve výchozím nastavení vypnuto)</span><span class="sxs-lookup"><span data-stu-id="fba17-122">Skip privacy settings (Off by default)</span></span>  <br/> |<span data-ttu-id="fba17-123">Pokud tato možnost nastavena na hodnotu **On**, zařízení uživatele při mu nejprve nezobrazí licenční smlouvy pro zařízení a Windows.</span><span class="sxs-lookup"><span data-stu-id="fba17-123">If this option is set to **On**, the device user will not see the license agreement for the device and Windows when he or she first signs in.</span></span>  <br/> |
|<span data-ttu-id="fba17-124">Nepovolit uživateli jako místní správce</span><span class="sxs-lookup"><span data-stu-id="fba17-124">Don't allow the user to become the local admin</span></span>  <br/> |<span data-ttu-id="fba17-125">Pokud tato možnost nastavena na hodnotu **On**, nebude moci instalovat jakékoli osobní apps, například Cortana zařízení uživatele.</span><span class="sxs-lookup"><span data-stu-id="fba17-125">If this option is set to **On**, the device user will not be able to install any personal apps, such as Cortana.</span></span>  <br/> |
   
