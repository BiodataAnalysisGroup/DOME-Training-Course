<p style='text-align: justify;'>
Machine learning models analyse experimental biological data by extracting patterns. The extracted patterns can then be used to give biological insights on similar data that were not previously seen by the model. The degree to which a model retains its performance on new data is called generalization power. Building ML models that generalize well is the main challenge of these methodologies, otherwise the trained models cannot be reused. Preprocessing data properly, and using it in a knowledgeable manner is the only way to obtain good generalization.
</p>

## 1.1 Provenance

- What is the __source__ of the data (database, publication, direct experiment)? 

- If data are in __classes__, how many data points are available in each class—for example, total for the positive (*Npos*) and negative (*Nneg*) cases? 

- If __regression__, how many real value points are there? 

- Has the dataset been __previously used__ by other papers and/or is it recognized by the community?


## 1.2 Dataset Splits

<p style='text-align: justify;'>
How many data points are in the training and test sets? Was a separate validation set used, and if yes, how large was it? Are the distributions of data types in the training and test sets different? Are the distributions of data types in both training and test sets plotted?</p>

## 1.3 Redundancy between data splits

<p style='text-align: justify;'>
 How were the sets split? Are the training and test sets independent? How was this enforced (for example, redundancy reduction to less than X% pairwise identity)? How does the distribution compare to previously published ML datasets?
 </p>

## 1.4 Availability of data

<p style='text-align: justify;'>
Are the data, including the data splits used, released in a public forum? If yes, where (for example, supporting material, URL) and how (license)?
</p>

## From Template

Here you can enter text and create inline citations[@Garcia2020] by using the bibtex plugin. Add your references in `references.bib`, and cite [@hoebelheinrich_nancy_j_2022_6769695] by adding the @refid inside brackets like this `[@10.1093/bioinformatics/btt113]`

You can also embed videos from a local source (with a relative path) or from an url (like youtube). To use a youtube URL, 
just attach the ID of the video to a youtube embedded video link: `https://youtube.com/embed/`. For example, the Elixir training video `https://youtu.be/oAD8FdGf8tI` has the ID `oAD8FdGf8tI`, so the final link would be:


!!! note "Note"

    Here you can put a note using admonitions.

    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.


!!! example "Exercise"
    This is a question

    ??? success "Solution"
        this is the soluiton to the question