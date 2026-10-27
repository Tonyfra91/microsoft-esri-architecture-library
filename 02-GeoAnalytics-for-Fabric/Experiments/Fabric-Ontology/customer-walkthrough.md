---
description: "Five-step customer walkthrough from Fabric capacity setup to an experimental Utility Network ontology proposal."
ms.date: 2026-10-27
ms.topic: how-to
---

# Customer Walkthrough: From Capacity to Ontology Evidence

Start in Fabric, provision compute in Azure if needed, return to Fabric to
assign that capacity to a workspace, then ask the ontology agent for a conceptual
proposal. This is the setup journey behind the
[V0 Conceptual Baseline](v0-conceptual-model.md), not an Asset Package import.

> [!IMPORTANT]
> This is experimental technical validation using preview functionality, not a
> native ArcGIS Utility Network integration. The existing screenshot records the
> V0 proposal only; it does not verify every setup step below. The walkthrough
> condenses Microsoft guidance checked on 2026-10-27 and has not been independently
> replayed in a live customer tenant. Preview labels and availability can change.

## The Five-Step Journey

![Five numbered steps: Fabric readiness, Azure capacity, workspace assignment, ontology proposal, and V0 evidence](../../images/fabric-ontology-experiment-walkthrough.png)

Repository-authored customer journey, not a Microsoft or Esri product
architecture. Five stages do not mean five clicks.
[Edit the diagram in draw.io](../../images/fabric-ontology-experiment-walkthrough.drawio).

## 1. Start in Fabric and Confirm Readiness

1. Sign in to [Microsoft Fabric](https://app.fabric.microsoft.com/) with your
   organizational account. Confirm the intended Microsoft Entra tenant.
2. Agree on a dedicated experiment workspace, owner, approved region, and cost
   limit. Use general terminology only for V0; do not upload customer utility data.
3. Ask the Fabric administrator to enable **Users can create Fabric items** and
   **Users can create ontology (preview) items** for the participants.
4. Confirm ontology-agent availability and the applicable Copilot permissions
   and regional processing settings with the administrator. Changes involving
   cross-region processing or subprocessors require organizational approval;
   do not enable them merely to dismiss an error.

Checkpoint: the tenant and owners are known, preview use is approved, and an
administrator can support capacity and agent configuration.

Sources: [ontology tenant settings](#supporting-microsoft-sources), sources 3
and 5 below.

## 2. Go to Azure and Create or Reuse Fabric Capacity

Capacity is the compute resource; the workspace is where the ontology item
lives. Creating one does not automatically configure the other.

1. If an approved, active capacity is already available, record its name and
   proceed to step 3. Do not buy a second capacity.
2. Otherwise, have an authorized owner open the
   [Azure portal](https://portal.azure.com/) in the same Entra tenant as Fabric.
   The Azure subscription must be associated with that tenant.
3. Search for **Microsoft Fabric**, then select **Create Fabric Capacity**.
4. Select the subscription, resource group, capacity name, approved region,
   size, and Fabric capacity administrator. Confirm `Microsoft.Fabric` resource
   provider registration and regional capacity-unit quota if provisioning is
   blocked.
5. Review pricing and obtain purchase approval before selecting
   **Review + create** and completing deployment. Confirm the capacity is active
   and record its name and administrator.

For this paid-capacity walkthrough, use an F SKU that supports the intended
agent experience. Microsoft's general Copilot guidance currently lists paid
F2 or higher, but that is not a sizing recommendation or a guarantee of
ontology-agent availability. Do not assume a Fabric trial or Power BI Pro/PPU
license alone enables the same experience. Confirm current feature, region,
and tenant requirements before purchasing.

Checkpoint: an active capacity exists in the correct tenant and approved region.

Sources: supporting sources 1 and 5 below.

## 3. Return to Fabric and Assign the Workspace

1. Return to [Microsoft Fabric](https://app.fabric.microsoft.com/). Under
   **Workspaces**, create a dedicated experiment workspace or open the agreed
   existing workspace.
2. Open **Workspace settings** and select **Workspace type**. Use **Edit** to
   choose the Fabric capacity workspace type and select the capacity from
   step 2, then apply the change. Some tenant experiences label this area
   **License info** or **License mode**.
3. Confirm the saved workspace settings show the intended capacity, not only
   a shared Power BI workspace type.
4. Give authors Contributor or higher workspace access. Have the workspace
   administrator and capacity owner handle assignment permissions if needed;
   Azure resource access alone is not workspace authoring access.

Checkpoint: the workspace is assigned to the intended active capacity and the
author can create Fabric items.

Source: supporting source 2 below.

## 4. Create an Ontology and Request a Conceptual Proposal

1. In the workspace, select **New item**, search for **Ontology (preview)**,
   and create an item with a name such as `EsriUtilityNetwork-V0`.
2. Open the empty item and select **Start with Ontology agent**. Keep the agent
   in **Plan** mode while reviewing its proposal.
3. Request a minimal conceptual model using general Utility Network terminology.
   Do not attach an Asset Package or claim schema grounding for this V0 exercise.
   The following is a suggested prompt, not a recovered transcript of the
   original experiment:

   ```text
   Propose a minimal conceptual ontology using general Esri ArcGIS Utility
   Network terminology. Suggest entity types, properties, and relationships
   for a small proof of concept. No Asset Package or authoritative Esri schema
   has been supplied. Label assumptions and unsupported concepts explicitly.
   Do not invent source data or bindings. Show the proposal for review only;
   do not apply or publish changes.
   ```

4. Review the proposed concepts and any stated evidence. If the agent requires
   sources before continuing, record that limitation rather than inventing data
   or claiming to reproduce V0. If unrelated sources are discovered, stop and
   correct the workspace scope.

Checkpoint: a reviewable conceptual proposal or an explicit blocker is recorded.
AI responses can vary; matching the original four entities is not an acceptance
test. Creating an empty ontology item is not the same as applying or publishing
a definition, and neither proves Esri schema validity.

Source: supporting source 4 below.

## 5. Capture V0 Evidence and Stop Before Grounding

1. Before approval or application, capture the proposal and its entity,
   property, and relationship details. Record the prompt, date, item name,
   workspace, capacity, and any warnings in approved experiment notes.
2. Compare the output with the
   [recorded V0 model and screenshot](v0-conceptual-model.md#evidence). Preserve
   differences rather than replacing historical evidence with a new response.
3. Save evidence before closing or refreshing the agent session. Do not include
   credentials or sensitive tenant/customer details in shared screenshots.
4. Stop at conceptual review. Asset Package inspection, source binding,
   Esri-domain validation, and any decision to apply or publish belong to the
   [V1 grounding phase](v0-conceptual-model.md#next-step-v1-asset-package-grounding).

Checkpoint: the proposal is traceable and clearly labeled as AI-generated,
unvalidated, and not a native integration.

After the session, have the capacity owner review costs. An authorized owner can
pause a dedicated F capacity in Azure when no one depends on it. Pausing affects
all workspaces on that capacity and can trigger settlement of outstanding
usage; it does not mean every associated charge disappears. Resume it before
the next session.

Sources: supporting sources 4 and 6 below.

## Common Setup Blockers

| Symptom                    | Check before continuing                                                     |
|----------------------------|-----------------------------------------------------------------------------|
| Capacity cannot be created | Azure permissions, provider registration, approved region, quota, and budget |
| Capacity is not listed     | Same Entra tenant, deployment/active state, and capacity assignment access    |
| Ontology item is missing   | Workspace capacity, author role, tenant settings, and preview availability    |
| Agent is unavailable       | Copilot configuration, capacity/region eligibility, and author permissions   |
| Proposal needs real data   | Record the blocker; do not invent sources or relabel the result as grounded  |

## Supporting Microsoft Sources

These references support the local walkthrough; they do not validate the Esri
conceptual model or prove that this experiment was executed end to end.

1. [Buy Fabric capacity](https://learn.microsoft.com/en-us/fabric/enterprise/buy-capacity):
   Azure prerequisites and capacity creation.
2. [Create and reassign a workspace](https://learn.microsoft.com/en-us/fabric/fundamentals/create-workspaces):
   workspace creation and assignment through Workspace type.
3. [Ontology required tenant settings](https://learn.microsoft.com/en-us/fabric/iq/ontology/overview-tenant-settings):
   Fabric and ontology item creation settings.
4. [Use the ontology agent](https://learn.microsoft.com/en-us/fabric/iq/ontology/how-to-use-ontology-agent):
   starting the agent, Plan/Act modes, proposal review, permissions, and sessions.
5. [Enable and configure Copilot](https://learn.microsoft.com/en-us/fabric/fundamentals/copilot-enable-fabric):
   capacity prerequisites, tenant controls, and regional processing considerations.
6. [Pause and resume Fabric capacity](https://learn.microsoft.com/en-us/fabric/enterprise/pause-resume):
   permissions, availability impact, and billing considerations.

Return to the [experiment overview](README.md) or continue with the
[V0 Conceptual Baseline](v0-conceptual-model.md).
