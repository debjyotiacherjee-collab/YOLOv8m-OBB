labels_master.csv is UTF-8 with BOM. Columns: filename,words,split,plate_id.
Resolve filename relative to the PARENT of this easyocr_finetuning_training folder.
words is blank on first generation. Fill only this column with the exact visible Bengali text.
These are WHOLE-PLATE crops from provided OBB annotations, not detected text-line crops.
For a line recognizer, create true text-line regions separately before recognition training.
No OCR recognition model is trained by this notebook. Never invent unreadable text.
All four variants inherit the source split and plate_id. Do not resplit individual CSV rows.
plate_id is a source-annotation identity, not a guarantee that two different photos show different physical plates.
Review identity/near-duplicate reports and use optional grouping overrides where known.
Rerunning unchanged preparation preserves words and backs up the old CSV. Close it in Excel first.
