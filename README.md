# Text-Generation-Using-RNN
Story generation system using RNN LM, Bigram LM, and HMM LM

In the initial pahse, 2 datasets are genertaed by collecting Shakespeare's story Othello and Macbeth.
Moreover, to generate a different style of story "Harry Potter and Philosopher's stone" story is collected to form a different dataset.
Data preprocessing steps are carried out to clean the raw input data.

Finally, three language models are implemented to generate different style stories.

TrailNgram.ipynb : Bigram language model is implemeneted here.
            Bigram models are trained using three datasets and the trained models are used to generate different kinds of stories.
            The text generation system is implemented in Python in Jupyter notebook. 
            create_bigram function can be invoked by passing the datasets to train the models.
            In the next stage, text can be generated using two approaches "Likely word" and "Random word".
            Likely Word: selects the next most probable word by considering the bigram grammar; only short length sentences can be generated using it. 
            Ranodm Word: To randomize the generated text. Cumulative probaility is computed on top of the bigram probability. Moreover, a random number between 0 and 1 is     generated, and the word that falls in the zone is considered as the next word in the sequence.
            
 RNNLM.ipynb: RNN language model is implemented here. The model is implemented in Python using TensorFlow library. A char-based RNN model that generates story from scratch is implemented as a part of this project. To train the model, create_LM function should be invoked passing the train dataset and the checkpoint directory as input.
 To generate story using the model, get_savedmodel should be invoked passing the input corpus and the checkpoint directory. Moreover, generate_text function should be invoked passing the desired length of characters to generate story of the desired length.
          
         
