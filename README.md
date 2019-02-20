#OpenIE Evaluation

A docker project for annotating OpenIE tupples. 

### Usage: 

For setting up the container and running it:
> ./setup.sh

For starting the server (when the pc is restarted):

> ./run-container.sh

Copying the data from the container to the local pc:

> ./get-results.sh

**Please**, check if the folder in the folder results is up to date after the call of the "get-results.sh". The way to do so is to go inside the folder of the language that you are annotating and check if the annotations are saved in the *.ann respective file.


**URL for the annotation:**
[http://localhost/brat-v1.3_Crunchy_Frog/#/]

Login: Username: **test**  Password:**test**

Pres TAB to open the selection of the files

#### Dataset:
When you open the url: [http://localhost/brat-v1.3_Crunchy_Frog/#/] with the "TAB" you can open the dialog. 

YOUR DATASET is under : evaluation/sentences/(your language code).


#### Annotations Guideline:

The goal is to annotate each sentence with tupples(propositions) of the form : Subject, Predicate, Object, Optional

There can be more than 1 tupple. So please, annotate each of the tupple in a different line.

When Annotating, please keep in mind two **rules**:
- Assertendness:
I.e:  in the sentence: *Sam succeeded in convincing John*

The annotation should be: Subject: **Sam**   ;  Predicate: **succeeded in convincing**	;  Object: **John** 

Or in *John could not join the band*: Subject: **John**     Predicate: **could not join**	Object: **the band** 


- Minimal Propositions:

I.e:  in the sentence: "Bell distributes electronics and building products"

The annotations should be: 
```
Subject: **Bell**     Predicate: **distributes**	Object: **electronic products** 
			   

Subject: **Bell**     Predicate: **distributes**	Object: **building products** 

```

**Important:** The Propositions are pieces of information that can *stand alone*  as a piece of information. 

##### English examples:

> ABS has formed a partnership with Habitat for Humanity to give a free Bible to each of its new homeowners in the United States .


```
Subject, *ABS*,  Predicate: *has formed*,  Object *a partnership with Habitat for Humanity*,  Optional: *to give a free Bible to each of its new homeowners in the US*

```


-  A.E. from Ulm is vegetarian.

```
Subject: *A.E.*,  Predicate : *is*,  Object: *vegetarian* 

Subject: *A.E. from Ulm*,  Predicate: *is*,  Object: *vegetarian*

Subject: *A.E.*,  Object: *from Ulm* 
```


- AE remained in Princeton until his death.

```
Subject: *AE*; Predicate: *remained*; Object: *In Princeton*; Optional: *until his death*

```


- Bell , a telecommunication company , which is based in Los Angeles , makes and distributes electronic , computer and building products .


```
Subject: *Bell*; **Predicate (doesn’t exist)** ; Object: **a telecommunication company.
> The meaning is: Bell is a telecomunication company


Subject: *Bell*; Predicate: *is based*; Object: *in Los Angeles*

Subject: *Bell*; Predicate: *makes*; Object: *electronic products*

Subject: *Bell*; Predicate: *makes*; Object: *computer products*

Subject: *Bell*; Predicate: *makes*; Object: *building products*


Subject: *Bell*; Predicate: *distributes* Object: *electronic products*

Subject: *Bell*; Predicate: *distributes* Object: *computer products*

Subject: *Bell*; Predicate: *distributes* Object: *building products*

```

- Andi went to the Know-Center and Konrad went to the institute.

```
Subject: *Andi* Predicate: *went*, object: *to the Know-Center*

Subject: *Konrad* predicate: *went*, object: *to the institute*

```

- AI is a subfield of Deep Learning.
```
Subject: *AI*, Predicate:*is a subfield of*, Object: *Deep Learning*
```

- Andi is a friend of Mario.
```
Subject: *Andi*, Predicate:*is a freind of*, Object: *Mario*
```


- He said that she went home earlier.

```
Subject: *He*, Predicate:*said*, Object: *she went home earlier* 

Subject: *she*, Predicate: *went*, Object:*home earlier*
```


**NOTE** there is also room for interpretation, like in the last example **earlier** might have been optional too!




 

