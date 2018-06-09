# Persuasion-Comments-Evaluation
1.Introduction

        Tensorflow Implementation of "Incorporating Argument-Level Interactions for Persuasion Comments Evaluation 
    using Co-attention Model". The dataset used in our paper can be download from the repository. 

2.Data Format

2.1 Dataset for persuasion comments evaluation(CMV)

        This directory CMV contains pairs of argumentative threads made in reply to the same original post, one 
    successful and one not (more details in Section 3.1 of our paper). Both files have the same format and store 
    data for training and heldout testing respectively. Each line is a json object for a pair. A pair has the 
    following fields:
        op_author, op_text, op_name, op_title, positive, negative.
    "positive" is a list of replies in a rooted path-unit that won a delta from OP, while "negative" is a matching 
    rooted path-unit that did not win a delta. "op_author", "op_text", "op_name" and "op_title" give information 
    for the original post.  
    
2.2 Annotated dataset for interactive argument pair extraction 

    The specific details of annotated dataset are in Section 4.1 of our paper. Here's an example of such a file:

    1
    ========Reply1========
    
    He cited this definition by Merriam-Webster: existing in nature and not made or caused by people: coming from 
    nature (URL) as his basis for the distinction for natural vs. unnatural. <<<===>>>Look at the definition you 
    provided, if we remove the exclusion of things which humans create: existing in nature and not made or caused 
    by people ~so essentially, by this definition, natural things are things that exist, which is frankly rather 
    meaningless.

    ========Reply2========
    
    He cited this definition by Merriam-Webster: existing in nature and not made or caused by people: coming from 
    nature (URL) as his basis for the distinction for natural vs. unnatural. <<<===>>> You're using natural to mean 
    definition 8 the universe, with all its phenomena. The more common definition is definition 1 the material world, 
    especially as surrounding humankind and existing independently of human activities. 

    He cited this definition by Merriam-Webster: existing in nature and not made or caused by people: coming from 
    nature (URL) as his basis for the distinction for natural vs. unnatural. <<<===>>> So by definition we are not 
    part of nature, as nature is more commonly used, and is in this sense used, to refer to things that exist 
    independently of human activities. 
    
    Notes:
        (1) Reply 1 and 2 indicate the positive reply and negative reply, respectively. 
        (2) The argument on the left of "<<<===>>>" is from original post and the argument on the right is from reply.
        (3) <<<===>>> indicates the interactive relationship.
 
    
3.Citation

    If you find the datasets useful, please cite the following paper: 
    
    @article{Ji2018Incorporating, title={Incorporating Argument-Level Interactions for Persuasion Comments Evaluation
    using Co-attention Model}, author={Lu Ji, Zhongyu Wei, Xiangkun Hu, Yang Liu, Qi Zhang and Xuanjing Huang}, 
    year={2018}, publisher={COLING} }.
    
    The detailed information about the paper will be released later.
    


