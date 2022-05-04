# DSE-309-Project

* Note *
The density plot in the 'Data Visualization' part may take a few seconds to execute.


* Note *
//
results = []
names = []
for name,model in models:
    kfold = KFold(n_splits = 10, random_state = None, shuffle = True)
    cv_result = cross_val_score(model, X_train, Y_train, cv = kfold, scoring = "accuracy")
    names.append(name)
    results.append(cv_result)
// 
This part of code takes quiet some time to execute. Do not quit the kernel and wait for few seconds.


* Note *
//
for i in range(len(names)):
    print(names[i], results[i].mean())
//
This part of code may give slightly different values different times. The difference in mostly
insignificant, but it should be noted. This may change the sns box plot a little. 
Also, there may be slight change in the values of classification report and confusion matrix but not much.
