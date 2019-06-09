<html>
<head>
<title>Assignment
</title>
</head>
<body bgcolor="LightGray">
<ul><li><h1 style="color:RED;font-size:35px;text-align:left;"> RIDGE REGRESSION</h1></li>
<P><font size='5'>Ridge regression is a way to create a parsimonious model <BR>
when the number of predictor variables in a set exceeds the number of observations,<br>
or when a data set has multicollinearity (correlations between predictor variables).</font></P>
<H2><font size="5">Ridge Regression vs. Least Squares</H2>
<P>Least squares regression isn’t defined at all when the number of predictors exceeds <br>the number of observations;
 It doesn’t differentiate “important” from “less-important” predictors in a model,<br> so it includes all of them. 
This leads to overfitting a model and failure to find unique solutions. Least squares<br> also has issues dealing 
with multicollinearity in data. Ridge regression avoids all of these problems. <br>It works in part because it doesn’t
 require unbiased estimators; While least squares produces unbiased estimates,<br> 
variances can be so large that they may be wholly inaccurate. Ridge regression adds just
enough bias to make the estimates reasonably reliable approximations to true population values.</P>
<H2>On Mathematics</H2>
OLS regression uses the following formula to estimate coefficients:

<br><B>B=(X'X)^-1X'Y<B><br>

If X is a centered and scaled matrix, the crossproduct matrix (X`X) is nearly singular when the X-columns are highly correlated. Ridge regression adds a ridge parameter (k),<br>
 of the identity matrix to the cross product matrix, forming a new matrix (X`X + kI). <br>It’s called ridge regression because the diagonal of ones in the correlation matrix can be described as a ridge. 
The new formula is used to find the coefficients:<br>

<br><B>B=(X'X+Ki)^-1X'Y<B></B><br>

Choosing a value for k is not a simple task,
which is perhaps one major reason why ridge regression isn’t used as much as least squares or logistic regression.

<H2>BENEFIT OF RIDGE REGRESSION</H2>
<UL><LI>The ridge regression line has small amount of bias due to penalty and has less variance.</li>
<li>The prediction made with the ridge regression line are less sensitive wieght than least square lines.</li></ul>

<li><H1 style="color:green;font-size:35px;text-align:left">LASSO REGRESSION</H1></LI>
<UL><LI>Performs L1 regularization, <BR>i.e. adds penalty equivalent to absolute value of the magnitude of coefficients</LI>
<LI>Minimization objective = LS Obj + a * (sum of absolute value of coefficients)</LI></UL>
<BR>Note that here ‘LS Obj’ refers to ‘least squares objective’,i.e. the linear regression objective without regularization.<BR>

If terms like ‘penalty’ and ‘regularization’ seem very unfamiliar to you, don’t worry we’ll talk about these in more <BR>
detail through the course of this article. Before digging further into how they work, lets try to get some intuition into <BR>
why penalizing the magnitude of coefficients should work in the first place.
<H2>THEORY</H2>
Lasso, or Least Absolute Shrinkage and Selection Operator, is quite similar conceptually to ridge regression.<BR>
 It also adds a penalty for non-zero coefficients, but unlike ridge regression which penalizes sum of squared<BR> 
coefficients (the so-called L2 penalty), lasso penalizes the sum of their absolute values (L1 penalty).<BR>
 As a result, for high values of ?, many coefficients are exactly zeroed under lasso, <BR>
which is never the case in ridge regression.<BR>
<LI><H1 style="color:Blue;font-size:35px;text-align:left">ELASTIC NET</H1></LI>
Elastic Net first emerged as a result of critique on lasso, whose variable selection can be too dependent on data<BR>
 and thus unstable. The solution is to combine the penalties of ridge regression and lasso to get the best of both worlds.<BR>
<BR>
Elastic net is basically a combination of both L1 and L2 regularization. So if you know elastic net,<BR>
 you can implement both Ridge and Lasso by tuning the parameters. So it uses both L1 and L2 penality term.</font><BR>
<H2 STYLE="COLOR:PURPLE;FONT-SIZE:25PX;TEXT-ALIGN:CENTER;">THANK YOU</H2>
<H2 STYLE="COLOR:BROWN;FONT-SIZE:25PX;TEXT-ALIGN:RIGHT;">NAME:RUPESH RANJAN KUMAR<BR>HML118</H2>
</body>
</html>
