search_terms.txt contains parameters used in searching data from webhose.io.

webhose_api_token.txt is token to access webnose.io.

action_words.csv contains verbs expressing threatening statement like kill, hurt, etc.

intention_ww.txt is part of training set.

new_posts2.txt is part of traning set.

Pipeline--Model Building.ipynb contains steps about how we built the pipeline including data collection, data manipulation, building action words filter and Threatening Statement Detection model.

Prediction.ipynb contains a example about how we applied the model in new data and made prediction.

results.json is the predicted results.

results.mtgl is the Maltego visualization of the results.json. (To open it, you need to download Maltego first)

If you want to regenerate the visualization, you can import hello.mtz after downloading Maltego and run transformation.

