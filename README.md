# Findings & Results

## SimpleCNN
- **Accuracy:** 80%  
- **Sensitivity (Recall for TB):** 64%  
- **Specificity:** 96%  
- **PPV (TB Precision):** 94%  
- **NPV (Healthy Precision):** 73%  
👉 Correctly identified most healthy cases but missed ~36% of TB cases.

---

## ResNet18 (Frozen Backbone)
- **Accuracy:** 76%  
- **Sensitivity (Recall for TB):** 54%  
- **Specificity:** 98%  
- **PPV (TB Precision):** 96%  
- **NPV (Healthy Precision):** 68%  
👉 Very precise when predicting TB but missed nearly half of the TB cases.

---

## ROC Curve (TB class)
- **SimpleCNN AUC = 0.92**  
- **ResNet18 AUC = 0.98**  
![ROC Curve](roc_curve.png)

---

## Key Takeaways
- Both models achieved high AUC, showing strong separation between TB and Healthy.  
- **SimpleCNN** had better recall for TB but weaker overall precision.  
- **ResNet18** achieved higher AUC and precision, but recall was lower when only the head was trained.  
- In medical settings, **Sensitivity matters most** — missing TB is riskier than false alarms.  
- With fine-tuning, ResNet18 could improve sensitivity further.

