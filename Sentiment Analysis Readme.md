# Movie-Rating-Prediction-RNN-with-use-of-callbacks

Aim:-
  Given the scraped data of movie reviews we had to find the label associated with review as positive or negative.
  
Data Preparation:-
  Train Data:-
    I have used the scrapped data from the IMDB official site and associated it with the positiveor negative review.
  Test Data:-
    Given the review we have to predict the sentiment associated with the review.
Model Planning:-
  So as to pre-process the data we have used the nltk pipeline which consist of following operations such tokenization,stopword removal,
  stemming and converting them into count vector form but here the issue was that every review was repersented by vocab size vector.
  To handle that we introduced a embedding layer so as to repersent every sentence in the vector of 300 dimension.
Model building:-
  After passing the input vector through embedding layer and before that padding every review to max size of 50 words so as fix the 
  RNN cell sizes, after passing it through the embedding layer our vector size came to (total_reviews*maxlen*300) and then it is passes
  through the RNN cells and in b/w the RNN cells the droupout layer was intoduced so as to make model more generalise.
  The output from final state vector is passed through sigmoid activation function and loss function as binarycrossentropy and optimizer
  as adam at the compile time.
  
Model enhancing and evaluating:-
