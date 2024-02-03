# rucode_d
Rucode festival 2023

This is the solution to the problem D from the Rucode Festival 2023. In this task, it was necessary to place accents in words.

This solution showed accuracy 92, but it could have been better, since there was a limit on the complexity of the model, I wrote a formula by which I estimated the complexity of the forest of decision trees and made a mistake in it.

The forumla was: number of parameters = nt * 2 ^ (dh + 1) <= 1_000_000, where nt - number of trees, dh - tree depth,  
but the correct one is: 2 ^ (dh + 1) <= 1_000_000, because catboost doesnt save all trees. 

The approximate accuracy should have been 95 if the model parameters were slightly corrected.

Dataset example:  
аа^к  
аа^ка  
аа^ке  
аа^ки  
аа^ков  
аа^ком  
аа^м  
аа^му  
аа^ничего  
аа^ничем  
ааро^не  
ааро^ловец  
ааро^новские  
