---
title: Custom Context Menu
permalink: /editor/custom-context-menu
---

# Custom Context Menu

## Header
    caf::PdmChildArrayField<RicCreateMultipleFracturesOptionItemUi*> m_options;

## Constructor

    CAF_PDM_InitFieldNoDefault(&m_options, "Options", "Options", "", "", "");
    m_options.uiCapability()->setUiEditorTypeName(caf::PdmUiTableViewEditor::uiEditorTypeName());
    m_options.uiCapability()->setCustomContextMenuEnabled(true);

## Usage

    void RiuCreateMultipleFractionsUi::defineCustomContextMenu(const caf::PdmFieldHandle* fieldNeedingMenu,
                                                           QMenu*                     menu,
                                                           QWidget*                   fieldEditorWidget)
    {
        caf::CmdFeatureMenuBuilder menuBuilder;

        menuBuilder << "RicMyFeature";
	    menuBuilder << "Separator";

    	menuBuilder.appendToMenu(menu);
	}
