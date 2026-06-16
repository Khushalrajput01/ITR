## CSS PART 1:-

# 8_ChromeDeveloperTool

        ChromeDeveloperTool is a built-in tool in the chrome browser used to inspect,test,and debug HTML,CSS,and JavaScript code of a webpage.

    Example:-

        press F12->inspect an element -> view or modify its HTML and CSS properties temporarily

# 9_CSS_Specificity

    CSS Specificity is the rule used by the browser to decide which CSS Style will be applied when multiple styles target the same element.

    Example:-
    CSS
        p{
            color: blue;
        }

        #para{
            color: red;
        }

    HTML
        <p id="para">Hello</p>

    Output:-
        The text color will be red because the ID selector (#para)has higher specificity than the element selector(p).

# 10_CSS_Border

    The CSS Border property is used to add a border around an HTML element.

    Syntax:-
        CSS

        border:width style color;

    Example:-
        CSS

        p{
            border:2px solid black;
        }

# 11_CSS_BoxModel

        The CSS BoxModel describes how the size of an HTML element is calculated . It consists of content,padding,border and margin.

        Example:-
            div{
                padding:10px;
                border:2px solid black;
                margin:15px;
            }

# 12_CSS_Margin_Collapsing

    1.Margin Collapsing occurs when the vertical margins of two adjacent elements touch each other.
    2.Instead of adding together,the browser uses only the larger margin

    Example:-
        .div1{
            margin-bottom:20px;
        }

        .div2{
            margin-bottom:30px;
        }

# 13_Inline_vs_BlockLevel

Inline Elements:-
    1.Occupy only the required width.
    2.Start on the same line.
    3.Example:-
        <span>,<a>.

Block-Level Elements:-
    1.Occupy the full available width.
    2.Start on a new line.
    3.Example:-
        <div>,<p>.

# 14_Image_Element

    The <img> element is used to display an image on a webpage.

    Example:-
        <img src="Flower.jpg" alt="Flower">

# 15_Inline_BlockDisplay

    The display: inline-block property makes an element behave like an inline element while allowing width,height,margin,and padding to be applied like a block element.

    Example:-
        span{
            display:inline-block;
            width:100px;
            height:50px;
        }

# 16_CSS_BoxSizing_BorderBox

    The box-sizing: border-box property includes the content,padding and border within the elements specified width and height.

    Example:-
        CSS

        div{
            width:200px;
            padding:20px;
            border:5px solid black;
            box-sizing:border-box;
        }

# 17_CSS_BrowserStyles_Reset

    A CSS Reset is used to remove the default styles(margin,padding,etc.)applied by browsers so that webpages look consistent across different browsers.

    Example:-
        CSS

        *{
            margin:0;
            padding:0;
            box-sizing:border-box;
        }

# 18_CSS_Inheritance

    CSS_Inheritance is a feature where child elements automatically inherit certain CSS properties from their parent elements.

    Example:-
    CSS

    body{
        color: blue;
    }

# 19_CSS_TextAlign

    The text-align property is used to align text horizontally within an element.

    Example:-
    CSS

    p{
        text-align:center;
    }

## CSS PART2

# 1_CSS_FontWeight

    The Font-Weight property is used to set the thickness(boldness)of text.

    Example:-
    CSS

    p{
        Font-Weight:bold;
    }

# 2_CSS_Pseudo_Classes

    CSS_Pseudo_Classes are keywords added to selectors to define a special state of an element.

    Example:-
    CSS
    
    a:hover{
        color:red;
    }

# 3_CSS_FirstChild & FirstOfTypePsuedoClasses

    :First_Child

    Selects an element if it is the First-Child of its parent.

    Example:-
    CSS

    p:First-Child{
        color:red;
    }

    :First_Of_Type

    Selects the first element of a specific type within its parent.

    Example:-
    CSS

    p:First-Of-Type{
        color:blue;
    }

# 4_CSS_nthChild

    The :nth-Child() pseudo-classes selects elements based on their position among sibling elements.

    Example:-
    CSS

    li:nth-Child(2){
        color: red;
    }

    This selects the 2nd <li> element.

# 5_Pseudo_More

    Pseudo-Classes are used to style elements in specific states or positions.

    Example:-
    CSS

    a:hover{
        color: red;
    }
    input:Focus{
        border:2px solid blue;
    }
    li:last-Child{
        color: green;
    }

# 6_CSS_PseudoElements

    CSS Pseudo-Elements are used to style a specific part of an element.

    Example:-
    CSS

    p::First_Letter{
        Font-Size:20px;
    }

    This styles the first letter of the paragraph.