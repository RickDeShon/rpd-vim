* Replace all text between two braces
%s/\s*{\_[^}]\{-}}/;/g

* deletes any trailing whitespace at the end of each line. If no trailing whitespace is found no change occurs, and the e flag means no error is displayed. 
:%s/\s\+$//e

* deletes any leading whitespace at the beginning of each line. 
:%s/^\s\+//e
" Same thing (:le = :left = left-align given range; % = all lines):
:%le

* Find string then delete to end of line
:%s/{pattern}.*//