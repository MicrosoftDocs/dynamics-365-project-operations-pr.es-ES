---
title: Configurar la contabilidad para proyectos internos
description: Este tema proporciona información sobre cómo configurar prácticas de contabilidad para proyectos internos en Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4085082"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="5c922-103">Configurar la contabilidad para proyectos internos</span><span class="sxs-lookup"><span data-stu-id="5c922-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="5c922-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="5c922-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5c922-105">Los proyectos internos permiten a las empresas realizar un seguimiento de los costos relacionados con las actividades que no se facturan a un cliente.</span><span class="sxs-lookup"><span data-stu-id="5c922-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="5c922-106">Ejemplos de proyectos internos incluyen:</span><span class="sxs-lookup"><span data-stu-id="5c922-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="5c922-107">Desarrollar un producto, como una aplicación móvil, y seguir el coste asociado con el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="5c922-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="5c922-108">Gestionar el tiempo y los gastos de preventa.</span><span class="sxs-lookup"><span data-stu-id="5c922-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="5c922-109">Este proyecto interno de preventa se puede convertir más tarde en un proyecto facturable si se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="5c922-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="5c922-110">Cualquier proyecto no asociado con un contrato en Dynamics 365 Project Operations se trata como interno.</span><span class="sxs-lookup"><span data-stu-id="5c922-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="5c922-111">Los perfiles de costes e ingresos del proyecto no se usan para determinar las reglas contables del proyecto.</span><span class="sxs-lookup"><span data-stu-id="5c922-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="5c922-112">El coste interno del proyecto siempre se registra utilizando principios de pérdidas y ganancias.</span><span class="sxs-lookup"><span data-stu-id="5c922-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="5c922-113">Las cuentas contables para contabilizaciones se definen en la página **Configuración de libro contable**.</span><span class="sxs-lookup"><span data-stu-id="5c922-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="5c922-114">Las transacciones de tiempo se contabilizan debitando la cuenta **Coste** y acreditando la cuenta **Asignación de nómina**.</span><span class="sxs-lookup"><span data-stu-id="5c922-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="5c922-115">Las transacciones de gastos se contabilizan debitando la cuenta **Coste** y acreditando la cuenta **Cuenta de contrapartida para gastos**.</span><span class="sxs-lookup"><span data-stu-id="5c922-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="5c922-116">Una vez que las transacciones se registran en el proyecto, si el proyecto está asociado con un contrato de proyecto, el sistema revierte todas las transacciones acumuladas y crea nuevas transacciones facturables.</span><span class="sxs-lookup"><span data-stu-id="5c922-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="5c922-117">Las transacciones facturables siguen las reglas de contabilidad definidas en el respectivo perfil de costos e ingresos del Proyecto.</span><span class="sxs-lookup"><span data-stu-id="5c922-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


