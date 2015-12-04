##CSS Tricks

![Coding](https://images.unsplash.com/photo-1429051883746-afd9d56fbdaf?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&s=a40432a29a1c55fc0b2ec7f1f2271877)

## ANIMATIONS

###WHAT IS A CSS3 ANIMATION?

An animation lets an element gradually change from one style to another.

You can change as many CSS properties you want, as many times you want.

####The @keyframes rule

When you specify CSS styles inside the @keyframes rule, the animation will gradually change from the current style to the new style at certain times.


	/* The animation code */
	
	@keyframes example {
	    from {background-color: red;}
	    to {background-color: yellow;}
	}

	/* The element to apply the animation to */

	div.squareanim {
	    width: 200px;
	    height: 200px;
	    margin:0 auto;
	    animation-name: example;
	    animation-duration: 4s;
	    animation-iteration-count: infinite;
	}
	

####BOUNCE EFFECT

We have here a tutorial of how to achieve the bounce effect.

View more animations [here](https://daneden.github.io/animate.css/)


![BounceEffect](http://i.imgur.com/qJ9dqft.jpg)

#####Let's take a look at the code:

/* The animation code */
		
		@keyframes fadeBounce {

			0% {
				opacity:0;
				transform:translateY(-200%);
			}

			40% {
				transform:translateY(0);
			}

			55% {
				transform: translateY(-6px);
			}

			70% {
				opacity:1;
				transform: translateY(0);
			}

			85% {
				transform:translateY(-3px);
			}

			100% {
				opacity:1;
				transform:translateY(0);
			}

		}

		/* The element to apply the animation to */

		.box-a {
			opacity: 0;
			animation-name: fadeBounce;
			animation-duration: 1s;
			animation-fill-mode: forwards;
			background-color: #e7eff5;
			padding: 20px 20px 0 20px;
			border: 2px solid #d3dee7;
			margin-bottom: 30px;
			box-shadow: 0px 5px 5px -2px rgba(0, 0, 0, .10);
			border-radius: 10px;
		}

		section.website-reference .boxes :nth-child(2) .box-a {
			animation-delay: .5s;
		}

		section.website-reference .boxes :nth-child(3) .box-a {
			animation-delay: 1s;
		}

		section.website-reference .boxes :nth-child(4) .box-a {
			animation-delay: 1.5s;
		}
		
We started by giving a name to our animation '@keyframes fadeBounce' and then linked to our element .box-a', by adding some properties like: 
	
	animation-name: fadeBounce;
	animation-duration: 1s;
	animation-fill-mode: forwards;
	
	
View Live Example [here](http://itsfranhere.github.io/CSSTricks/#/wbref)


####MAKING IT SIMPLE

	animation: fadeBounce 1s forwards;	
	-webkit-animation: fadeBounce 1s forwards;(Chrome & Safari)
	
CSS vendor prefixes or CSS browser prefixes are a way for browser makers to add support for new CSS features in a sort of testing and experimentation period.

There is much more like:

	-o (opera)
	-moz (mozilla)
	-ms (Internet Explorer)


####CHANGING THE DURATION

	animation: fadeBounce 5s forwards;
	-webkit-animation: fadeBounce 5s forwards;
	
View Live Example [here](http://itsfranhere.github.io/CSSTricks/#/wbref2)

	
####CHANGE THEIR BEHAVIOUR
	
	animation-iteration-count: infinite;
	animation-direction: alternate;
	
	The first property is going to make the animation infinite, so it doesn't stop.
	
	The second one is going to reverse the cycle or alternate the duration.
	
View Live Example [here](http://itsfranhere.github.io/CSSTricks/#/wbref3)

![CssTricksPresentation](http://i.imgur.com/zqq810I.png)

View whole Presentation [here](http://itsfranhere.github.io/CSSTricks)