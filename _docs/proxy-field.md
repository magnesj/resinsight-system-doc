---
title: Proxy Field
permalink: /field/proxy
layout: default
---

# Proxy Field

A proxy field is used for derived data, often a name of an object. This data is not stored to project file, and a function is called when the user interface requires data to be displayed.

## Header
    caf::PdmProxyValueField<QString>         m_nameAndItemCount;

    QString                         nameAndItemCount() const;

## Constructor
    CAF_PDM_InitFieldNoDefault(&m_nameAndItemCount, "NameCount", "Name", "", "", "");
    m_nameAndItemCount.registerGetMethod(this, &RimSummaryCaseCollection::nameAndItemCount);

