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

Cras non vestibulum quam. Nulla venenatis tempor porttitor. Aenean `interdum` augue faucibus feugiat rhoncus. *Pellentesque habitant morbi*{:.underline} *tristique senectus et* netus **et malesuada fames ac turpis** egestas. Nunc eu purus id diam auctor gravida. Morbi ut mollis nisl. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Sed elementum metus nec arcu auctor, sed blandit ipsum dapibus. Donec quis ante vitae risus rhoncus euismod. Vestibulum eu arcu et turpis posuere convallis. Morbi gravida arcu sit amet metus consequat cursus. Phasellus id eros suscipit lorem lobortis elementum. Etiam lectus est, lacinia id consectetur et, vehicula a lorem. Integer justo lacus, facilisis eu volutpat sed, convallis sed metus. Fusce ligula ipsum, mollis nec bibendum eget, aliquam ac ante [^1].

> People go on about places like Starbucks being unpersonal and all that, but what if that's what you want? I'd be lost if people like that got their way and there was nothing unpersonal in the world. I like to know that there are big places without windows where no one gives a shit. You need confidence to go into small places with regular customers... I'm happiest in the Virgin Megastore and Borders and Starbucks and Pizza Express, where no one gives a shit and no one knows who you are. My mum & dad are always going on about how soulless those places are, and I'm like Der. That's the point.
> 
> <cite>Stephen King</cite>

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

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean convallis sem eget risus convallis consectetur. In non nisi augue. Aliquam nec lorem eget velit facilisis sollicitudin. Aenean in luctus neque. Mauris malesuada, elit at luctus posuere, diam dolor eleifend quam, maximus blandit diam lectus ut turpis. Integer sed ligula ac metus vulputate tincidunt a sit amet purus. Mauris in feugiat est. Morbi sit amet maximus lacus. Sed condimentum quam a sodales mattis. Fusce euismod tristique velit a ornare. Sed ac velit ligula.

Nullam efficitur, ex id luctus mattis, neque leo egestas odio, sit amet cursus nisl est eu nisl. Curabitur ut volutpat enim. Nunc consequat a dui ac dictum. Sed dictum interdum nulla, sit amet gravida arcu pretium at. Praesent vestibulum ante quis neque malesuada, vitae consequat nulla iaculis. Quisque sed sem arcu. Pellentesque maximus ultrices volutpat. Fusce imperdiet ligula nec risus dapibus, sit amet porta nisi finibus.

1. Apples are red.
2. Organges are orange.
3. Grapes are sometimes purple.
4. Watermelon is green on the outside and red on the inside.

Ut rhoncus leo feugiat felis ultricies elementum. Quisque gravida enim ut nulla rhoncus, blandit aliquam ante sollicitudin. Cras condimentum, leo ac malesuada consectetur, mi erat consectetur ipsum, nec sagittis enim risus ac ex. Nam et nisl ut erat mollis sollicitudin. Nullam eu nisi vitae lacus consequat porta. Duis dictum elit a sapien vulputate lobortis. Donec consectetur venenatis lacus a pharetra. Sed nec urna sit amet ex tempor ultricies a sodales neque. Nullam molestie tempor ultrices. Aliquam sit amet tellus ac nunc scelerisque hendrerit a eu tortor. Cras placerat libero ac hendrerit sollicitudin. Vivamus ut sodales neque. Sed vulputate efficitur leo sit amet sagittis.

Nulla condimentum eu velit eu sodales. Mauris eu nibh tincidunt, lobortis erat rutrum, efficitur sem. In hac habitasse platea dictumst. Mauris rutrum leo et augue dictum, a tempor urna mattis. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam venenatis elit odio, at commodo nisl vestibulum ac. Integer porttitor turpis nec dui consequat faucibus. Mauris non varius quam.

Curabitur sed tristique quam. Pellentesque ac interdum eros. Sed efficitur auctor ipsum a aliquet. Aenean facilisis erat non egestas tempus. Nulla nec nulla a felis bibendum convallis id at est. Morbi posuere nisl et ex vehicula placerat. Donec egestas massa lectus, sed egestas lorem blandit sit amet. Aliquam dapibus vitae nisi et euismod. Maecenas a turpis a nunc condimentum luctus vel nec est. Integer hendrerit erat et luctus dignissim.

Sed lobortis hendrerit purus eu ornare. Maecenas vitae nulla ut tellus pharetra accumsan vel et enim. Duis semper turpis lectus, nec elementum metus cursus quis. Donec turpis nibh, euismod in elit ac, lacinia laoreet massa. Sed efficitur nisl a eleifend mollis. Ut sed est id orci vestibulum lobortis. Ut eu metus scelerisque, egestas elit at, porta velit. Maecenas semper leo a lorem fermentum, non dignissim enim aliquam. Donec tempor sodales metus, vel viverra dui pellentesque in. Sed mattis mi et quam eleifend aliquam. Aliquam et leo felis.

In finibus nunc sit amet tellus maximus pellentesque. Maecenas erat mi, mattis quis vulputate sed, interdum vel enim. Sed maximus vulputate porttitor. Vestibulum at bibendum ligula, in aliquam magna. Sed tincidunt, dolor pretium bibendum eleifend, urna enim scelerisque neque, vitae luctus metus libero quis enim. Fusce hendrerit fringilla rhoncus. Donec volutpat augue quis malesuada rhoncus. Vestibulum tristique libero et orci ullamcorper tincidunt. Aliquam erat volutpat. Mauris varius enim lectus, non dictum felis condimentum imperdiet. Nulla leo metus, sollicitudin quis bibendum quis, volutpat at nisi.

Nam mattis ullamcorper eros sed suscipit. Aenean vehicula massa arcu, ac tincidunt felis bibendum ut. Sed et fringilla quam. Donec rhoncus aliquam eleifend. Nam vitae congue erat. Nunc vel porttitor nunc, non pellentesque ligula. Nullam iaculis condimentum velit, a vehicula metus mollis nec. Donec vel elementum metus. Aliquam erat volutpat. Maecenas a erat sit amet lorem posuere accumsan. Suspendisse potenti. Etiam ante magna, pretium id massa sed, ultrices varius magna. Maecenas egestas mi sed lorem mattis, in sodales eros iaculis. Mauris convallis urna vel ipsum dignissim placerat.

Curabitur laoreet sem ac velit viverra, non porta felis volutpat. Nunc accumsan, dolor at commodo dignissim, neque justo ullamcorper sem, ac sollicitudin orci tortor vel velit. Vivamus consequat nisl quis ligula vehicula, eu placerat justo porttitor. Aenean rutrum vestibulum mattis. Cras molestie augue ex, id faucibus odio dignissim at. Aenean sit amet consectetur risus. Pellentesque non tellus eu nisi tempor porta eget ac elit. Morbi sit amet nisi nunc. Nunc feugiat libero eu rhoncus mollis. Donec ultricies luctus ligula varius ultricies. Curabitur auctor lorem nec augue faucibus facilisis eget pulvinar sem. Proin in massa quis enim pulvinar porta quis ac urna. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

Fusce euismod erat non leo pretium convallis. In lorem tellus, gravida quis fringilla sit amet, tristique ac leo. Aliquam ac nunc neque. Pellentesque vehicula risus at sem dapibus malesuada. Quisque aliquet vel dui mollis condimentum. Nullam eu libero pretium, consectetur purus non, bibendum neque. Nulla facilisi. Nullam in enim vitae dui tempor pharetra. Nullam eget massa tellus. Donec sit amet porta leo. Pellentesque maximus efficitur sodales. Donec sit amet felis mattis, mattis lectus a, ultricies risus. Duis tincidunt sem id ex volutpat, nec hendrerit urna vehicula.

Fusce cursus velit ut magna luctus, sed aliquet nulla congue. Curabitur quis nibh condimentum, pretium metus et, elementum risus. Suspendisse non ipsum vel erat semper tincidunt. Aliquam pretium iaculis lacus, quis varius lectus consequat et. Etiam lobortis quam pharetra odio dignissim lobortis. Aliquam lorem dui, convallis ac purus vel, commodo gravida quam. Ut id dolor id velit venenatis porttitor. Etiam fringilla ullamcorper diam, hendrerit placerat lacus facilisis a. Pellentesque tincidunt posuere tristique. Vivamus posuere nec nisi feugiat placerat. Phasellus fermentum sapien eget lorem sollicitudin, eget elementum quam tincidunt. Pellentesque tincidunt congue risus vitae tempus. Donec imperdiet justo at luctus varius. In hac habitasse platea dictumst.

Ut eget nulla egestas, pharetra nunc ac, efficitur felis. Etiam non diam ac ipsum porta pretium vel nec est. Integer massa ante, iaculis vel nisl vitae, malesuada mollis purus. Curabitur justo orci, porttitor vel accumsan tincidunt, venenatis at ex. Morbi ac est nisi. Praesent tincidunt tempor quam sed bibendum. Fusce lobortis commodo posuere. Quisque id laoreet magna, in laoreet nisl. Donec quam nisi, feugiat viverra porttitor at, placerat id libero. Interdum et malesuada fames ac ante ipsum primis in faucibus. Aenean nulla velit, accumsan eget commodo ultricies, laoreet vel nunc. Nunc a vestibulum urna, ut porttitor velit.

Nullam in finibus mi, ac vestibulum risus. Ut vel felis pulvinar, congue sem semper, sagittis lorem. Etiam egestas est eu mi laoreet, eu tincidunt metus tristique. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ipsum quam, scelerisque lobortis pretium vitae, commodo sed purus. Donec posuere diam quis pellentesque vehicula. Morbi at semper sapien. Nullam in mi at libero porta rhoncus id vitae nisi. Donec nisl tortor, suscipit non neque in, convallis bibendum tortor. Vivamus ut mi imperdiet, dictum enim id, aliquet lectus.

Pellentesque vel ipsum neque. Nullam nunc nunc, faucibus eu mi ac, pulvinar rhoncus nunc. Nunc hendrerit elit a ligula porta, eget euismod enim venenatis. Phasellus a commodo felis. Mauris consequat pulvinar eros. Vestibulum aliquet neque vel purus fringilla luctus. Donec dictum, tortor eu vestibulum sollicitudin, metus elit varius erat, gravida fermentum quam orci id enim. Quisque risus quam, malesuada tristique posuere accumsan, iaculis quis leo. Praesent urna nisi, posuere nec massa ut, tempor faucibus libero.

Fusce in dictum diam. Phasellus tempor aliquam nibh et malesuada. Ut commodo interdum felis, suscipit dictum eros commodo at. Praesent sed lacus metus. Suspendisse dapibus mollis turpis, eu mollis erat tincidunt sed. Quisque elementum id purus vel euismod. Quisque id ornare purus, ut varius ipsum. Donec ut eros sed massa scelerisque dictum. Donec ac commodo dolor. Vestibulum pretium condimentum est vel rutrum. Donec felis risus, tempus id imperdiet at, viverra eget nibh. Quisque non tincidunt erat. Phasellus sit amet lorem ac lectus sodales suscipit id sollicitudin quam.

Mauris laoreet lacinia facilisis. Maecenas sit amet lacinia mauris. Nunc et fermentum tortor. Integer at euismod tellus. Suspendisse ornare vitae sem a consectetur. Proin ullamcorper tellus aliquam sem semper, non tempor arcu iaculis. Pellentesque mattis, sapien vitae venenatis pulvinar, dui neque interdum massa, in convallis neque dui eget lacus. Proin sollicitudin, nibh a pharetra faucibus, est tortor suscipit magna, sed tempus nibh arcu nec felis. Morbi bibendum ipsum convallis sem commodo fringilla. Mauris ultrices velit ut risus gravida, in interdum dolor semper. Mauris vehicula purus sed euismod auctor. Mauris congue fringilla tempor. Phasellus vulputate turpis mi, sed dictum ligula placerat sit amet.

Suspendisse ac erat eu ligula eleifend mattis quis lacinia orci. Maecenas vulputate magna ac ultricies tempor. Nam eu odio vitae neque viverra sollicitudin a vitae nunc. Fusce mauris dolor, mollis a eros id, dictum luctus diam. Aenean egestas tortor egestas, lobortis massa a, faucibus erat. Duis imperdiet risus eget lorem pulvinar sollicitudin. Sed tortor purus, aliquam ac tincidunt quis, bibendum at urna. Ut facilisis tellus libero, vestibulum consectetur est egestas in. Mauris semper velit non feugiat placerat. Praesent porttitor porta mi vel tincidunt. Morbi eget tincidunt elit. Vivamus condimentum elit enim, vitae auctor odio maximus at.

Curabitur porta quis ex at faucibus. Nullam malesuada, ligula nec porttitor volutpat, massa diam consequat felis, at viverra lectus enim eu nisl. Curabitur ac magna posuere dui consectetur gravida vitae at nunc. Aliquam ultricies et nunc a venenatis. Fusce sodales rutrum diam id pulvinar. Etiam a pretium diam, vel dignissim ante. Nulla fringilla metus nibh, ac dictum ante aliquam vel. Phasellus vel blandit est. Nullam dignissim felis at sem suscipit mattis. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Vivamus et feugiat tortor. Interdum et malesuada fames ac ante ipsum primis in faucibus. Mauris vehicula ex ut augue pretium tincidunt. Fusce at libero eget felis vulputate suscipit a vitae tellus. Sed sollicitudin sapien varius, imperdiet velit et, tempus ipsum.

Vivamus et sollicitudin elit, nec pellentesque velit. Mauris a massa id neque commodo feugiat. Sed diam justo, sagittis tempor nunc sed, pellentesque ullamcorper ante. Nunc at egestas nunc. Maecenas blandit sodales purus, vel porta nisl semper at. Maecenas fermentum bibendum mauris placerat tempus. Vestibulum ut orci felis. Nulla et massa et orci dignissim molestie. Vestibulum ornare est sed elit dapibus convallis.

Ut in enim iaculis, elementum ex at, venenatis erat. Vivamus congue, arcu vel lacinia malesuada, ex magna lacinia mauris, in mollis sapien diam maximus nisi. Cras convallis, nunc vel iaculis ultricies, nisi leo posuere lectus, sit amet ultrices urna velit ut nulla. Donec hendrerit dolor et malesuada ullamcorper. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Aliquam vulputate faucibus iaculis. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nunc posuere lacinia lacus a rutrum. Maecenas faucibus eros at leo convallis pellentesque. Phasellus vulputate, velit egestas varius pulvinar, nisl orci varius nibh, eu semper dolor odio vel diam. In orci velit, molestie non aliquam quis, rutrum quis leo. Praesent sodales eros vel interdum rutrum. Nunc quis odio sed orci scelerisque finibus in non enim. Donec consectetur non nisl nec aliquet.

[^1]: This has something to do with something.