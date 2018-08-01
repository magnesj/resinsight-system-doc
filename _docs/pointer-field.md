---
title: Pointer Field
permalink: /pointer-field
layout: default
---

# Pointer Field

## Definition

caf::PdmPtrField<RimWellPath*> m_parentWell;

## Implentation

### Constructor
    CAF_PDM_InitFieldNoDefault(&m_parentWell, "ParentWell", "Parent Well", "", "", "");

```cpp
QList<caf::PdmOptionItemInfo> RimWellPathGeometryDef::calculateValueOptions(const caf::PdmFieldHandle* fieldNeedingOptions, 
                                                                             bool* useOptionsOnly)
{
    QList<caf::PdmOptionItemInfo> options;

    if (fieldNeedingOptions == &m_wellStartType)
    {
        options.push_back(caf::PdmOptionItemInfo("Start at First Target",RimWellPathGeometryDef::START_AT_FIRST_TARGET  ));
    }

    return options;
}
```

