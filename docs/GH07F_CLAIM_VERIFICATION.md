# GH.07F — Controlled claim verification

This stage establishes a three-label claim verification **test harness** for synthetic FD-100 facts. It is not a learned NLI model. It only recognizes reviewed exact English propositions and refuses to decide on unseen claims. Evidence is bound to the reviewed synthetic text hash as well as registry integrity.

Labels: SUPPORTED, CONTRADICTED, INSUFFICIENT. All results keep semantic_verified=False. No changes to frozen GH.07 or GH.07B datasets. This code does not modify the production answer path.

Next steps: independent labeled NLI dataset, model calibration, threshold and abstention analysis, independent document registry, safety review, integration with proposed answer generation. Public release HOLD.
