---
layout: post
title: Markdown Styling
author: Stephen Czekalski
description: This post acts as a testing ground for styling markdown.
---

Before learning about Jekyll and static-site generators, I had a wordpress website. Wordpress is big, and,
on my cheap shared web hosting plan, it was slow. But I could deal with that. My main issue with it, and the
primary reason I switched to Jekyll, 

### Paragraphs
{: class="padding-t-s"}
Lorem ipsum dolor sit amet, consectetur adipiscing elit. [Quisque semper](http://www.google.com) mi quis turpis accumsan pulvinar. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Vestibulum vitae ante sit amet justo fringilla pellentesque. Mauris bibendum urna sed neque rhoncus faucibus. Aliquam aliquet faucibus tortor, vitae tristique libero ullamcorper ac. Aliquam erat volutpat. Quisque pellentesque sit amet lacus sit amet tincidunt. Vestibulum volutpat massa et dapibus feugiat. Integer vel pulvinar mauris. Donec eu arcu ac mi sollicitudin semper vel non risus. Aliquam erat volutpat.

Cras non vestibulum quam. Nulla venenatis tempor porttitor. Aenean `interdum` augue faucibus feugiat rhoncus. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Nunc eu purus id diam auctor gravida. Morbi ut mollis nisl. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Sed elementum metus nec arcu auctor, sed blandit ipsum dapibus. Donec quis ante vitae risus rhoncus euismod. Vestibulum eu arcu et turpis posuere convallis. Morbi gravida arcu sit amet metus consequat cursus. Phasellus id eros suscipit lorem lobortis elementum. Etiam lectus est, lacinia id consectetur et, vehicula a lorem. Integer justo lacus, facilisis eu volutpat sed, convallis sed metus. Fusce ligula ipsum, mollis nec bibendum eget, aliquam ac ante.

Praesent viverra consectetur mollis. Aenean finibus quam et neque malesuada, laoreet molestie magna molestie. Donec ornare, elit non molestie tincidunt, magna lacus ultricies magna, a pulvinar justo diam eu nisl. Morbi sagittis odio augue, a tristique nulla sagittis quis. Morbi eget condimentum sapien. Nullam libero purus, bibendum non imperdiet eget, pretium vel sapien. Mauris a efficitur risus. Aenean nisl libero, placerat ac magna ut, pellentesque bibendum metus. Duis fermentum iaculis libero, sodales pretium lectus mollis auctor. Phasellus ornare vitae tortor sed rutrum. Fusce condimentum sem vel tincidunt auctor. Sed dolor orci, hendrerit non lectus eget, gravida consectetur turpis. Sed congue tincidunt purus, eget consectetur augue pulvinar dignissim. Pellentesque placerat purus at ullamcorper dapibus. Curabitur et orci quam. Quisque in semper quam.

Nulla facilisi. Donec tristique massa id suscipit laoreet. Aliquam ut mi tellus. Donec dapibus luctus ipsum, consequat scelerisque quam sodales condimentum. In hac habitasse platea dictumst. Etiam eu interdum nunc. Sed eget cursus arcu. Vivamus lobortis ac tortor nec venenatis. `Kramdown::Document.new(text).to_html` Quisque dapibus lobortis urna quis ultrices. Aliquam eu rhoncus est. Morbi convallis fermentum lectus, at mattis nisl gravida ac.

Nullam et odio et nunc consectetur pulvinar at at dui. Vestibulum at commodo nibh, eu tincidunt nisl. Aenean accumsan nunc velit, efficitur tincidunt erat tristique nec. Etiam tempor augue vitae mollis blandit. Praesent tincidunt orci tortor, congue fermentum est gravida quis. Sed gravida justo nec luctus porta. Duis sit amet enim quis arcu ornare porttitor quis ac nibh. Vestibulum metus augue, fringilla ac augue malesuada, tempor rutrum felis. Fusce sagittis ullamcorper efficitur. Morbi mattis ligula in sagittis blandit. Donec non nibh non sem laoreet finibus sed vitae sem. Praesent sit amet rutrum erat. Nullam magna lacus, commodo vitae porta eget, ultricies in nunc.

~~~ python
# Import the modules
import sys
import random

ans = True

while ans:
    question = raw_input("Ask the magic 8 ball a question: (press enter to quit) ")
    
    answers = random.randint(1,8)
    
    if question == "":
        sys.exit()
    
    elif answers == 1:
        print "It is certain"
    
    elif answers == 2:
        print "Outlook good"
    
    elif answers == 3:
        print "You may rely on it"
    
    elif answers == 4:
        print "Ask again later"
    
    elif answers == 5:
        print "Concentrate and ask again"
    
    elif answers == 6:
        print "Reply hazy, try again"
    
    elif answers == 7:
        print "My reply is no"
    
    elif answers == 8:
        print "My sources say no"
~~~

### Blockquotes
{: class="padding-t-s"}

> Get busy living or get busy dying.
>
> <cite>Stephen King</cite>
