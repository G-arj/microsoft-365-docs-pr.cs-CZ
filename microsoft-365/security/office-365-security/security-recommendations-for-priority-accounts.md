---
title: Doporučení zabezpečení pro prioritní účty v Microsoft 365, prioritní účty, prioritní účty v Office 365, prioritní účty v Microsoft 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
audience: Admin
ms.topic: conceptual
ms.date: ''
ms.localizationpriority: medium
search.appverid:
- MET150
- MOE150
ms.assetid: ''
ms.collection:
- M365-security-compliance
- m365solution-overview
- m365solution-protecthve
ms.custom: ''
description: Správci se  dozvěděli, jak zvýšit úroveň nastavení zabezpečení a používat sestavy, upozornění a vyšetřování pro prioritní účty ve Microsoft 365 organizacích.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: f27e146df680b36c117816f0a07e45e0345c647a
ms.sourcegitcommit: b3530441288b2bc44342e00e9025a49721796903
ms.translationtype: MT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/20/2022
ms.locfileid: "63675409"
---
# <a name="security-recommendations-for-priority-accounts-in-microsoft-365"></a>Doporučení zabezpečení pro prioritní účty v Microsoft 365

Ne všechny uživatelské účty mají přístup ke stejným informacím o společnosti. Některé účty mají přístup k citlivým informacím, jako jsou finanční data, informace o vývoji produktů, přístup partnerů k důležitým build systémům a další. V případě ohrožení zabezpečení představují účty, které mají přístup k vysoce důvěrným informacím, vážné ohrožení. Tyto typy účtů nazýváme _prioritními účty_. Mezi prioritní účty patří (ale nejsou omezeny) ředitelé, SNSO, finanční ředitelé, účty správců infrastruktury, účty systému buildů a další.

Pro útočníky jsou běžné útoky phishing, které vrhaly náhodnou síť pro běžné nebo neznámé uživatele, neefektivní. Útoky útoku _phishing_ nebo _lovu_ velryb, které se zaměřují na prioritní účty, jsou pro útočníky velmi přínosné. Účty s prioritou proto vyžadují silnější ochranu než běžná ochrana, aby se zabránilo ohrožení zabezpečení účtu.

Microsoft 365 a Microsoft Defender pro Office 365 obsahují několik klíčových funkcí, které poskytují další vrstvy zabezpečení pro vaše prioritní účty. Tento článek popisuje tyto možnosti a jak je používat.

![Shrnutí doporučení zabezpečení ve formuláři ikon](../../media/security-recommendations-for-priority-users.png)

|Úloha|Všechny Office 365 Enterprise plány|Microsoft 365 E3|Microsoft 365 E5|
|---|:---:|:---:|:---:|
|[Zvýšení zabezpečení přihlášení u prioritních účtů](#increase-sign-in-security-for-priority-accounts)|![Zahrnuto.](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![Zahrnuto.](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![Zahrnuto.](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|[Použití striktně přednastavených zásad zabezpečení pro účty s prioritou](#use-strict-preset-security-policies-for-priority-accounts)|![Zahrnuto.](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![Zahrnuto.](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![Zahrnuto.](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|[Použití značek uživatelů u účtů s prioritou](#apply-user-tags-to-priority-accounts)|||![Zahrnuto](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|[Monitorování účtů s prioritou v upozorněních, sestavách a zjišťováních](#monitor-priority-accounts-in-alerts-reports-and-detections)|||![Zahrnuto](../../media/d238e041-6854-4a78-9141-049224df0795.png)|
|[Trénovat uživatele](#train-users)|![Zahrnuto.](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![Zahrnuto](../../media/d238e041-6854-4a78-9141-049224df0795.png)|![Zahrnuto](../../media/d238e041-6854-4a78-9141-049224df0795.png)|

> [!NOTE]
> Informace o zabezpečení _privilegovaných účtů_ (účtů správců) najdete v [tomto tématu](/azure/architecture/framework/security/critical-impact-accounts).

## <a name="increase-sign-in-security-for-priority-accounts"></a>Zvýšení zabezpečení přihlášení u prioritních účtů

Prioritní účty vyžadují vyšší zabezpečení přihlášení. Zabezpečení přihlášení můžete zvýšit tak, že budete vyžadovat vícefaktorové ověřování (MFA) a zakážete starší ověřovací protokoly.

Pokyny najdete v [kroku 1. Zvyšte zabezpečení přihlášení pro vzdálené pracovníky pomocí MFA](../../solutions/empower-people-to-work-remotely-secure-sign-in.md). I když se tento článek týká vzdálených pracovníků, stejné koncepty platí pro prioritní uživatele.

**Poznámka**: Důrazně doporučujeme globálně zakázat starší ověřovací protokoly pro všechny uživatele s prioritou, jak je popsáno v předchozím článku. Pokud vám to vaše obchodní požadavky brání, Exchange Online nabízí následující ovládací prvky, které vám pomůžou omezit rozsah starších ověřovacích protokolů:

- Zásady [ověřování a pravidla](/exchange/clients-and-mobile-in-exchange-online/disable-basic-authentication-in-exchange-online) klientského [](/exchange/clients-and-mobile-in-exchange-online/client-access-rules/client-access-rules) přístupu můžete v aplikaci Exchange Online použít k blokování nebo povolení základních ověřovacích protokolů a starších ověřovacích protokolů, jako jsou protokoly POP3, IMAP4 a ověřený protokol SMTP pro konkrétní uživatele.

- Přístup pomocí protokolu POP3 a IMAP4 můžete zakázat u jednotlivých poštovních schránek. Ověřený protokol SMTP můžete zakázat na úrovni organizace a povolit ho u konkrétních poštovních schránek, které ji stále vyžadují. Pokyny najdete v následujících článcích:
  - [Povolení nebo zakázání přístupu pomocí protokolu POP3 nebo IMAP4 pro uživatele](/exchange/clients-and-mobile-in-exchange-online/pop3-and-imap4/enable-or-disable-pop3-or-imap4-access)
  - [Povolení nebo zakázání odeslání ověřeného klienta SMTP (SMTP AUTH)](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission)

Je také dobré poznamenat, že základní ověřování se v Exchange Online pro Exchange Web Services (EWS), protokol Exchange ActiveSync, POP3, IMAP4 a vzdálený PowerShell nepoužívá. Podrobnosti najdete v tomto [příspěvku na blogu](https://developer.microsoft.com/office/blogs/deferred-end-of-support-date-for-basic-authentication-in-exchange-online/).

## <a name="use-strict-preset-security-policies-for-priority-accounts"></a>Použití striktně přednastavených zásad zabezpečení pro účty s prioritou

Prioritní uživatelé vyžadují přísnější akce pro různé ochrany, které jsou dostupné v Exchange Online Protection (EOP) a Defenderu pro Office 365.

Například místo doručování zpráv klasifikovaných jako spam do složky Nevyžádaná pošta byste měli stejné zprávy umístit do karantény, pokud jsou určené pro prioritní účty.

Tento přísný přístup k účtům s prioritou můžete implementovat pomocí profilu Strict v přednastavených zásadách zabezpečení.

Přednastavené zásady zabezpečení jsou praktické a centrální umístění, kde můžete použít naše doporučená přísná nastavení zásad pro všechny ochrany v EOP a Defenderu pro Office 365. Další informace najdete v tématu [Přednastavené zásady zabezpečení v EOP a Microsoft Defenderu pro Office 365](preset-security-policies.md).

Podrobnosti o tom, jak se nastavení zásad Strict liší od výchozího a standardního nastavení zásad, najdete v tématu Doporučená nastavení pro [EOP a Microsoft Defender pro Office 365 zabezpečení](recommended-settings-for-eop-and-office365.md).

## <a name="apply-user-tags-to-priority-accounts"></a>Použití značek uživatelů u účtů s prioritou

Uživatelské značky v programu Microsoft Defender pro Office 365 Plán 2 (jako součást předplatného Microsoft 365 E5 nebo doplňku) jsou způsob, jak rychle identifikovat a klasifikovat konkrétní uživatele nebo skupiny uživatelů v sestavách a vyšetřování incidentů.

**Prioritní účty** jsou typ předdefinované značky uživatele (označované jako systémová _značka), kterou_ můžete použít k identifikaci incidentů a upozornění, které zahrnují prioritní účty. Další informace o účtech **s prioritou** najdete v tématu [Správa a sledování prioritních účtů](../../admin/setup/priority-accounts.md).

Můžete také vytvořit vlastní značky, které budou dál identifikovat a klasifikovat vaše prioritní účty. Další informace najdete v tématu [Uživatelské značky](user-tags.md). Účty s **prioritou** (systémové značky) můžete spravovat ve stejném rozhraní jako vlastní uživatelské značky.

## <a name="monitor-priority-accounts-in-alerts-reports-and-detections"></a>Monitorování účtů s prioritou v upozorněních, sestavách a zjišťováních

Po zabezpečení a označení prioritních uživatelů můžete pomocí dostupných sestav, upozornění a vyšetřování v EOP a Defenderu pro Office 365 rychle identifikovat incidenty nebo zjišťování, které zahrnují prioritní účty. Funkce, které podporují značky uživatelů, jsou popsané v následující tabulce.

|Funkce|Popis|
|---|---|
|Upozornění|Značky uživatelů, kterých se to týká, jsou viditelné a dostupné jako filtry na stránce **Upozornění** na Microsoft 365 Defender portálu. Další informace najdete v tématu [Zobrazení upozornění](../../compliance/alert-policies.md#viewing-alerts).|
|Průzkumník <p> Zjišťování v reálném čase|V **Průzkumníkovi** (Defender for Office 365 Plan 2) nebo v reálném čase (Defender for Office 365 Plan 1) jsou značky uživatelů viditelné v zobrazení mřížky e-mailu a v plovoucím panelu Podrobnosti **e-mailu**. Značky uživatelů jsou k dispozici také jako vlastnost, která je možné filtrovat. Další informace najdete v tématu  [Značky v Průzkumníkovi](threat-explorer.md#tags-in-threat-explorer).|
|Zobrazení kampaně|Uživatelské značky jsou jednou z mnoha filtrovatelných vlastností v zobrazeních kampaní v programu Microsoft Defender Office 365 Plán 2. Další informace najdete v tématu [Zobrazení kampaní](campaigns.md).|
|Zpráva o stavu ochrany před hrozbou|Prakticky ve všech zobrazeních a tabulkách podrobností v sestavě stavu ochrany před hrozbou můžete výsledky filtrovat podle **účtů priority**. Další informace najdete v článku [Zpráva o stavu ochrany před hrozbou](view-email-security-reports.md#threat-protection-status-report).|
|E-mailové problémy pro sestavu prioritních účtů|Sestava **Problémy s e-mailem pro** prioritní účty v Centru pro správu Exchange (EAC) obsahuje informace o nedoručovaných a zpožděných zprávách pro **prioritní účty**. Další informace najdete v článku o [problémech s e-mailem pro sestavu prioritních účtů](/exchange/monitoring/mail-flow-reports/mfr-email-issues-for-priority-accounts-report).|

## <a name="train-users"></a>Trénovat uživatele

Školicí uživatelé s prioritními účty můžou uživatelům a vašemu týmu bezpečnostních operací ušetřit hodně času a frustrace. Důvtipní uživatelé mají menší pravděpodobnost, že otevřou přílohy nebo kliknou na odkazy v sporných e-mailových zprávách, a s větší pravděpodobností se vyhne podezřelým webům.

Příručka k kampani [kyberbezpečnostní](https://www.belfercenter.org/CyberPlaybook) kampaně na harvardské škole Pro Školy pro kybernetickou bezpečnost poskytuje vynikající pokyny k vytvoření silné kultury informovanosti o zabezpečení ve vaší organizaci, včetně školení uživatelů k identifikaci útoků phishing.

Microsoft 365 poskytuje následující zdroje informací, které pomáhají informovat uživatele ve vaší organizaci:

|Koncept|Zdroje|Popis|
|---|---|---|
|Microsoft 365|[Přizpůsobitelné výukové dráhy](/office365/customlearning/)|Tyto materiály vám můžou pomoct s přípravami pro uživatele ve vaší organizaci.|
|Microsoft 365 zabezpečení|[Učení: Zabezpečte svou organizaci pomocí integrovaného inteligentního zabezpečení před Microsoft 365](/learn/modules/security-with-microsoft-365)|Tento modul umožňuje popsat, jak Microsoft 365 funkce zabezpečení spolupracují, a vytyčovat výhody těchto funkcí zabezpečení.|
|Vícefaktorové ověřování|[Dvoukroková ověření: Co je další ověřovací stránka?](/azure/active-directory/user-help/multi-factor-authentication-end-user-first-time)|Tento článek pomáhá koncovým uživatelům pochopit, co je vícefaktorové ověřování a proč se používá ve vaší organizaci.|
|Školení k simulaci útoků|[Začínáme používat školení k simulaci útoku](attack-simulation-training-get-started.md)|Školení k simulaci útoků v Microsoft Defenderu pro Office 365 Plán 2 umožňuje správci konfigurovat, spouštět a sledovat simulované útoky phishing proti konkrétním skupinám uživatelů.|

Kromě toho společnost Microsoft doporučuje uživatelům provádět akce popsané v tomto článku: Chraňte svůj účet a zařízení [před hackery a malwarem](https://support.microsoft.com/office/066d6216-a56b-4f90-9af3-b3a1e9a327d6). Mezi tyto akce patří:

- Použití silných hesel
- Ochrana zařízení
- Povolení funkcí zabezpečení na Windows a macech (pro nespravovaná zařízení)

## <a name="see-also"></a>Viz také

[Oznámení o ochraně prioritních účtů v programu Microsoft Defender pro Office 365](https://techcommunity.microsoft.com/t5/microsoft-defender-for-office/announcing-priority-account-protection-in-microsoft-defender-for/ba-p/1696385)
