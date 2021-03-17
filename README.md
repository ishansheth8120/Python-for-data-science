{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Basics of Python\n",
    "\n",
    "Fill valid code/values in place of blanks. "
   ]
  },
  {
   "cell_type": "raw",
   "metadata": {},
   "source": [
    "# Demo\n",
    "# initialize variable 'msg' with the string 'Hello World'\n",
    "msg = string\n",
    "\n",
    "# Solution\n",
    "msg = \"Hello World\""
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# initialize variables 'a' and 'b' with 5 and 6 respectively\n",
    "a = 5 \n",
    "b = 6\n",
    "\n",
    "# add 'a' and 'b' and assign the result into a new variable 'c'\n",
    "c = a + b\n",
    "print(c)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# build a function to add 2 numbers\n",
    "def addition(x,y):\n",
    "    return(x + y)\n",
    "\n",
    "# use the function 'addition' to add 'a' and 'b'\n",
    "addition(a, b)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# create a list consisting of first 5 even numbers and print the list\n",
    "my_list = [2,4,6,8,10]\n",
    "print(my_list)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# access the 3rd element of the list 'my_list'\n",
    "my_list[2]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# given below is a dictionary having 4 unique keys, i.e., 'name', 'age', 'gender', 'is_employed'\n",
    "my_dict = {'name':'Smith',\n",
    "           'age':34,\n",
    "           'gender': 'Male',\n",
    "           'is_employed': False}\n",
    "\n",
    "# print 'my_dict'\n",
    "print(my_dict)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# access value under 'name' key from 'my_dict'\n",
    "my_dict['name']"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# update 'is_employed' key to True\n",
    "my_dict.update({'is_employed':True})\n",
    "\n",
    "# print the updated dictionary\n",
    "print(my_dict)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# use a for loop to print only even numbers from the first 20 numbers, i.e. 1-20\n",
    "for i in range(1,21):\n",
    "    if i % 2 == 0:\n",
    "        print(i)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Please download the file \"data_python.csv\"."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "# import required libraries\n",
    "import pandas as pd\n",
    "import numpy as np"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "## read data_python.csv using pandas\n",
    "mydata = pd.read_csv(\"data_python.csv\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "## print the number of rows and number of columns of mydata\n",
    "mydata.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "## assign a variable 'target' with the 'Loan_Status' feature from mydata dataframe\n",
    "target = mydata['Loan_Status']"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "## print the datatype of ApplicantIncome feature\n",
    "print(mydata['ApplicantIncome'].dtypes)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "## conditional statement - print 'Yes' if the 21st element of 'Education' feature is 'Graduate' else print 'No'\n",
    "if(mydata['Education'][21] == 'Graduate'):\n",
    "    print('yes')\n",
    "else:\n",
    "    print('no')   "
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "## print 31st to 35th rows of mydata\n",
    "mydata.iloc[31:36]"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {
    "collapsed": true
   },
   "outputs": [],
   "source": [
    "## print first 5 rows of 2nd and 3rd column only\n",
    "mydata.iloc[:5,[1,2]]"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.6.0"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}


