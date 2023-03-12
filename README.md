# Image-Classification-Using-SIFT-BOVW-SVM-and-Random-Forests

\abstract{In this assignment, Image Classification is performed using the concept of Bag of Visual Words as the feature extractor followed by 2 different classifiers i.e., Support Vector Machines and Random Forests. The feature descriptor used is Scale-Invariant Feature Transform (SIFT). The algorithm is evaluated on 2 different data sets. The performance is quantified using metrics like Accuracy Score, F-1 Score, True Positive Rates, and True Negative Rates.}

section{Methodology}\label{sec1}

Image Classification is a computer vision problem that involves assigning label(s) to an image based on its features. Bag of Visual Words is an image classification technique that represents an image as a histogram of local features of the image. The feature descriptors are extracted using different feature extractors like SIFT, SURF, BRISK, etc. The one used in this task is SIFT. \\
Clustering Algorithm is then applied to the feature descriptors to define the vocabulary. KMeans is applied for this purpose. The centers of these clusters are the visual words in the vocabulary or the codebook. \\
Now, each image can be represented as the frequency of the visual words present in the image. This frequency is found by creating histograms for each image. This histogram representation of each image is then fed into the classifiers along with their true labels to train the classifier. When any new image is being tested, the image is first converted into the histogram representation which is then fed into the classifier to make a prediction.\\
The classifiers used are Support Vector Machines and Random Forests. In this report, the effectiveness of Bag of Visual Words with SVMs and Random Forests for image classification is explored using two different data sets that are discussed in the next section. We compare the performance using metrics like accuracy, f1 score, true positive rates, and false positive rates which are discussed in the third section along with some correctly and incorrectly predicted images.


\section{Data Sets}\label{sec2}
Two Data Sets have been used in this task. 
\begin{itemize}
    \item The first dataset contains object images with 4 classes: Soccer Ball, Accordion, Dollar Bill, and MotorBike. The train set and test set has already been split. The train set contains 14 images per class making a total of 56 images, and the test set contains 2 images per class making a total of 8 images.
    \item The second dataset contains a total of 3670 flowers images with 5 classes: daisy (633 images), dandelion (898 images), roses (641 images), sunflowers (699 images), and tulips (799 images). The train set and test set is split by using the train\textunderscore test\textunderscore split function from sklearn.
\end{itemize} 

\section{Results}\label{sec3}
The evaluation metrics used are Accuracy score, F1 score, true positive rate (TPR), and false positive rate (FPR). The classifiers are Support Vector Machines (SVM) and Random Forests (RF).
\begin{itemize}
    \item Objects Data Set
    \begin{table}[h]
        \begin{center}
        \begin{tabular}{|c|c|c|c|c|}
        \hline
        \textbf{} &\textbf{\textit{Accuracy}}& \textbf{\textit{F1-Score}}& \textbf{\textit{TPR}}& \textbf{\textit{FPR}} \\
        \hline
        SVM & 75.0 & 74.2 & 75.0 & 8.32  \\
        \hline
        RF & 75.0 & 73.3 & 75.0 & 8.32  \\
        \hline
        \end{tabular}
        \end{center}
    \end{table}
    \item Flowers Data Set
    \begin{table}[h]
        \begin{center}
        \begin{tabular}{|c|c|c|c|c|}
        \hline
        \textbf{} &\textbf{\textit{Accuracy}}& \textbf{\textit{F1-Score}}& \textbf{\textit{TPR}}& \textbf{\textit{FPR}} \\
        \hline
        SVM & 59.1 & 57.4 & 57.1 & 10.4  \\
        \hline
        RF & 56.1 & 53.8 & 54.0 & 11.1  \\
        \hline
        \end{tabular}
        \end{center}
    \end{table}
\end{itemize}

\newpage
\subsection{Few Correct and Incorrect Predictions}
\begin{itemize}
    \item Objects Data Set
    \begin{figure}[h]
        \centering
        \includegraphics[width=10cm]{obj_svm1.jpg}
        \includegraphics[width=10cm]{obj_svm2.jpg}
        \caption{\centering SVM predictions}
        \label{fig:my_label}
    \end{figure}
    \begin{figure}[h]
        \centering
        \includegraphics[width=10cm]{obj_rf1.jpg}
        \includegraphics[width=10cm]{obj_rf2.jpg}
        \caption{\centering RF predictions}
        \label{fig:my_label}
    \end{figure}

    \newpage
    \item Flowers Data Set
    \begin{figure}[h]
        \centering
        \includegraphics[width=12cm]{fl_svm1.jpg}
        \includegraphics[width=12cm]{fl_svm2.jpg}
        \caption{\centering SVM predictions}
        \label{fig:my_label}
    \end{figure}
    \begin{figure}[h]
        \centering
        \includegraphics[width=12cm]{fl_rf1.jpg}
        \includegraphics[width=12cm]{fl_rf2.jpg}
        \caption{\centering RF predictions}
        \label{fig:my_label}
    \end{figure}
\end{itemize} 

\newpage
\section{Conclusion}
Overall, it can be seen that since the Objects dataset was pretty small so the performance has been better in comparison to the Flowers dataset. Moreover, a surprising result was seen that Support Vector Machines performed similarly if not better than Random Forests. All in all, it can be said that Bag of Visual Words is a fairly good algorithm for image classification.

\section{Links}
\hyperlink{}{GitHub repository} \\
\hyperlink{https://www.overleaf.com/read/sqqpvgqvdvpb}{Overleaf Report}

