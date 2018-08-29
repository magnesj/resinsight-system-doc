# Header file
    
    caf::PdmField< bool >   m_pickPointsEnabled;
    
# Constructor
  
    CAF_PDM_InitField(&m_pickPointsEnabled, "m_pickPointsEnabled", false, "", "", "", "");
    caf::PdmUiPushButtonEditor::configureEditorForField(&m_pickPointsEnabled);
    
# FieldChangedByUI

    if (changedField == &m_pickPointsEnabled)
    {
        if (m_pickPointsEnabled)
        {
            // Do command stuff
        }
        
        // If it is supposed to be a push button, reset it
        m_pickPointsEnabled = false;
    }
    
# defineEditorAttribute
    
    caf::PdmUiPushButtonEditorAttribute* pbAttribute = dynamic_cast<caf::PdmUiPushButtonEditorAttribute*> (attribute)
    pbAttribute->m_buttonText = "Stop picking points";
