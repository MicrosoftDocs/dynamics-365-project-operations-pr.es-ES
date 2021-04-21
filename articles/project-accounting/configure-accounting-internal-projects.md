---
title: Configurar la contabilidad para proyectos internos
description: Este tema proporciona información sobre cómo configurar prácticas de contabilidad para proyectos internos en Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857999"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="7e35b-103">Configurar la contabilidad para proyectos internos</span><span class="sxs-lookup"><span data-stu-id="7e35b-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="7e35b-104">_**Se aplica a:** Project Operations para escenarios basados en recursos/no en existencias_</span><span class="sxs-lookup"><span data-stu-id="7e35b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7e35b-105">Los proyectos internos permiten a las empresas realizar un seguimiento de los costos relacionados con las actividades que no se facturan a un cliente.</span><span class="sxs-lookup"><span data-stu-id="7e35b-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="7e35b-106">Ejemplos de proyectos internos incluyen:</span><span class="sxs-lookup"><span data-stu-id="7e35b-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="7e35b-107">Desarrollar un producto, como una aplicación móvil, y seguir el coste asociado con el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="7e35b-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="7e35b-108">Gestionar el tiempo y los gastos de preventa.</span><span class="sxs-lookup"><span data-stu-id="7e35b-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="7e35b-109">Este proyecto interno de preventa se puede convertir más tarde en un proyecto facturable si se gana la oferta.</span><span class="sxs-lookup"><span data-stu-id="7e35b-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="7e35b-110">Cualquier proyecto no asociado con un contrato en Dynamics 365 Project Operations se procesa como interno.</span><span class="sxs-lookup"><span data-stu-id="7e35b-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="7e35b-111">Los perfiles de costes e ingresos del proyecto no se usan para determinar las reglas contables del proyecto.</span><span class="sxs-lookup"><span data-stu-id="7e35b-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="7e35b-112">El coste interno del proyecto siempre se registra utilizando principios de pérdidas y ganancias.</span><span class="sxs-lookup"><span data-stu-id="7e35b-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="7e35b-113">Las cuentas contables para contabilizaciones se definen en la página **Configuración de libro contable**.</span><span class="sxs-lookup"><span data-stu-id="7e35b-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="7e35b-114">Las transacciones de tiempo se contabilizan debitando la cuenta **Coste** y acreditando la cuenta **Asignación de nómina**.</span><span class="sxs-lookup"><span data-stu-id="7e35b-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="7e35b-115">Las transacciones de gastos se contabilizan debitando la cuenta **Coste** y acreditando la cuenta **Cuenta de contrapartida para gastos**.</span><span class="sxs-lookup"><span data-stu-id="7e35b-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="7e35b-116">Las transacciones de elementos se registran cargando en la cuenta **Coste** y abonando en la cuenta **Coste - Elemento**.</span><span class="sxs-lookup"><span data-stu-id="7e35b-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="7e35b-117">Una vez que las transacciones se registran en el proyecto, si el proyecto está asociado a un contrato de proyecto, el sistema revierte todas las transacciones acumuladas y crea nuevas transacciones facturables.</span><span class="sxs-lookup"><span data-stu-id="7e35b-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="7e35b-118">Las transacciones facturables siguen las reglas de contabilidad definidas en el respectivo perfil de costos e ingresos del Proyecto.</span><span class="sxs-lookup"><span data-stu-id="7e35b-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
