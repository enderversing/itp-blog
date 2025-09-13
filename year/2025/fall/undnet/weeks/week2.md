# Week 2



## Readings

### On Distributed Communications



This is the paper talking about the design of the Internet as a network that could survive military attacks! So fascinating.


What is adaptive store-and-forward? Is it possible for store-and-forward routed devices to have permanent memory without a centralized server or "cloud"? The idea of recent history of network traffic being used to modify path selection reminds me of the design of the Solar Protocol. 

When I learned of the Solar Protocol's design, I found it naive, but some of what I found naive is similar to how the Internet works. I always assume that everything in the human world, hardware or software, has been meticulously designed using esoteric algorithms and data structures. I am shocked when I turn out to be wrong.*


I wonder why "a standard format message block" would enable real-time voice over Internet? Meshtastic is a radio network that uses store-and-forward routing but struggles to enable voice transmission of any kind, let alone real time.

I will always find the distributed network more beautiful than the decentralized network. Maybe I'm simple. There's a kind of purity of thought and simplicity there which I find very appealing.

I am not sure how the minimum span of a network is related to the decentralized network's "redundancy level". (Frankly, I'm still not sure what the minimum span is.)

I love talking about noise. Information theory, here we go!** 

I'm really excited to have this reference because, even more than the content in the piece, I'm happy to concretely be able to point to an example of how military operations shaped the development of the Internet. I have read about or around this subject, but never have I accessed a primary source of this nature.

Why do switching systems need to try a subset of potential paths that can be drawn on a gridded network? I may be misunderstanding the problem here, but couldn't these paths be predicted? If there is a need to try paths instead of using an algorithm to predict them, I would suspect that switching is actually a computationally difficult problem?


-   We will soon be living in an era in which we cannot guarantee survivability of any single point. However, we can still design systems in which system destruction requires the enemy to pay the price of destroying n of n stations. If n is made sufficiently large, it can be shown that highly survivable system structures can be built—even in the thermonuclear era.
    



I think this piece is shortsighted, but probably written with the best foresight the author could imagine in their time. Right now, we see "system destruction" from time to time in the form of outages. I can only imagine these outages become more and more bombastic if or when quantum computers become less noisy***.

I have been reading a book with a great title - *Why Hackers Win* - which discusses how the Internet is actually becoming more centralized, and therefore, less stable, as time progresses.~*


#### Footnotes

*I like when I find complexity in the design of everyday "things". I was reading books about music last week and a few of them mentioned the design of the MP3 as a compression format designed to be transported over networks. I always assume that all digital creations are complex or wordlessly deep.

**I still don't really understand information theory, I've just read the first chapter of one highly esteemed book on the subject over and over.

***Quantum computers could be the end of the Internet, or merely the next coming of dishonest tech startups - I'm not sure yet.

~*Tom, if you are reading this - I assume you know that an Arduino was used to hack, or expose, a serious vulnerability in the  wireless auto-ignition and keyless entry systems used by almost every Volkswagen car since 1995 (via the hacking book, published a while ago). How do you feel about that? Thoughts?

### Stupid Networks

Honestly, I don't understand this piece. What is the stupid protocol? Is it...the Internet? How is the Internet stupid?

## Testing DJ's Droplet

I was struggling to get myself to start my homework for this week. I had to create a new droplet because my old droplet was deleted (probably compromised because of my poorly configured firewall). 

I wonder if I can penetration test DJ's droplet while I wait for my own droplet traffic to materialize. I was thinking I might remember the password he shared in class from memory, but I checked his Notion and a password is still there, in plaintext.

Do not worry about my intentions - I am an ethical white hat penetration testing knight in shining armor. I'm simply educating the people. 

---

``` 
ssh root@104.248.225.197
kex_exchange_identification: read: Connection reset by peer
Connection reset by 104.248.225.197 port 22
```

Well, that's interesting. I'll log in as a different user on his droplet.

```
ssh sudosudofreak@104.248.225.197
kex_exchange_identification: read: Connection reset by peer
Connection reset by 104.248.225.197 port 22
```

Is this droplet alive? 
```
ping 104.248.225.197
PING 104.248.225.197 (104.248.225.197): 56 data bytes
Request timeout for icmp_seq 0
Request timeout for icmp_seq 1
Request timeout for icmp_seq 2
Request timeout for icmp_seq 3
Request timeout for icmp_seq 4
Request timeout for icmp_seq 5
Request timeout for icmp_seq 6
Request timeout for icmp_seq 7
Request timeout for icmp_seq 8
Request timeout for icmp_seq 9
Request timeout for icmp_seq 10
^C
--- 104.248.225.197 ping statistics ---
12 packets transmitted, 0 packets received, 100.0% packet loss
```
100% packet loss suggests that his droplet is down. I think we both struggled setting up our firewalls.

