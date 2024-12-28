---
title: "Marks"
date: 2024-12-29T00:14:56+08:00
draft: false
---

So a few months back, I was in a Marks and Spencer in London looking for a drink when I noticed a something rather peculiar. The M&S was selling a 350ml bottle of a pineapple, banana, and coconut smoothie for £2.60, while I found the exact same pineapple, banana and coconut smoothie in a 750ml bottle for £2.20. My first instinct was that they had mislabelled the prices, but these two bottles were found in different parts of the store, so that was unlikely the case. I wasn’t complaining I guess, I was looking for a full drink since I had run out of water in my bottle. Nonetheless I was hesitant of buying the 750ml bottle. It felt too good to be true, almost illegal. How can you possibly get more than double the drink for less money?

I sought to find an answer to this problem, and so I turned to my followers on Instagram to give me a good economic answer. And I did get a pretty good answer, namely economies of scale, where it is actually cheaper per unit volume to produce larger containers which use relatively less plastic. But of course, I was bored and I started learning microeconomics, and now, half a year later, I can give a more detailed answer to this problem.

Just want to preface that the following content may contain a lot more math than the average person can appreciate, so read at your own will.

### Groundwork

There are a few factors at play in this scenario, namely:

1. economies of scale
2. market segmentation
3. product differentiation
4. price discrimination
5. information asymmetry

Firstly, as described above, it is cheaper per millilitre for the packaging of larger bottles rather than smaller bottles, resulting in economies of scale. In the market, we can identify two types of consumers, one that is more willing to pay higher prices for the convenience of a smaller bottle of drink, and one that is more price sensitive and would rather buy in bulk, this is market segmentation in play. In response to this, M&S has done product differentiation by size, by selling the same product (smoothie) in two different sizes, the smaller 350ml bottle and the larger 750ml bottle. Price discrimination goes hand in hand with this, allowing M&S to sell the smoothie at different prices depending on the consumer’s willingness to pay. Finally, there is also information asymmetry, as the small 350ml bottle is right at the front of the shop, while the 750ml bottle is tucked away somewhere in the back, making the smaller bottle much more visible.

We shall attempt to model this through an economic lens. We will be making some assumptions to ensure a feasible model, however, we will also try to model the factors listed above. For the sake of simplicity, we shall consider a market of smoothies sold in arbitrary units of volume, where a small bottle is 1 unit, and a large bottle is 2 units.  We also want to assume that M&S is a monopolist in the market, able to set the price of the drinks to maximise revenue. Let us begin by modelling the costs of producing the different bottles, and the two different types of consumers.

### Modelling consumption and costs

Let’s first begin by modelling costs. We assume that the total cost of production by M&S consists of three parts. There is a fixed cost $C_f$, a variable cost from producing small bottles $C_s$, and a variable cost in producing large bottles $C_\ell$. We can express this as a function of the quantity of drink produced by small bottles $q_s$ and large bottles $q_\ell$.

$$
C(q_s, q_\ell)=c_f+C_s(q_s)+C_\ell(q_\ell)
$$

We define $C_s$ and $C_\ell$ as consisting of the packaging cost and the product cost. The packaging cost is proportionate to the surface area of the bottle, while the product cost is proportionate to the volume of smoothie. For packaging, we assume the two bottles are square bottles with fixed base but variable height. The total surface area of the small bottle can be written as

$$
A_s=2d^2+4dh
$$

where $a$ is the length of one of the square sides of the base and $h$ is the height. Also note that the volume $V$ can be given as

$$
V=d^2h\\\Rightarrow h=\frac{V}{d^2}
$$

This allows us to write the surface area as

$$
A_s=2d^2+\frac{4V}{d}
$$

We can then find the surface area for the large bottle by doubling the value of $V$.

$$
A_\ell=2d^2+\frac{8V}{d}
$$

We still have to scale the surface area of the large bottle down by half, to factor in the per unit volume by which we are considering production. This allows us to get the packaging cost per unit volume. The final variable cost functions are shown below.

$$
C_s(q_s)=q_s[c_{\text{pack}}(\frac{2d^2}{V}+\frac{4}{d})+c_{\text{prod}}]\\C_\ell(q_\ell)=q_\ell[c_{\text{pack}}(\frac{d^2}{V}+\frac{4}{d})+c_{\text{prod}}]
$$

Now we can start modelling consumption. We assume that the market consists of two types of consumers. Consumer 1 is the person on the go, valuing convenience over cost. Consumer 1 is willing to spend more for the convenience of small bottles, however, they are still influenced by price and would buy large bottles if the price of small bottles is unreasonable. Consumer 2 on the other hand is the more price sensitive buyer. They are indifferent to the container size, and only purchase based on the volume of smoothie.

To represent the consumers, we start off with base demand functions below. $Q_1$ and $Q_2$ are the quantity demanded for consumers 1 and 2 respectively, $P$ is the price, with the other variables being constants.

$$
Q_1(P)=a_1-b_1P\\\\ Q_2(P)=a_2-b_2P
$$

For consumer 1, we would like to separate the demand function into related demands for small bottles and large bottles. For the small bottles, we shall introduce a convenience factor $c_{\text{conv}}$ which models the buyer’s preference. This results in the following functions.

$$
Q_{1,s}(P_s)=a_1-b_1(P_s-c_{\text{conv}})\\Q_{1,\ell}(P_\ell)=a_1-b_1P_\ell
$$

We do the same for consumer 2, however we do not need to modify the function between bottle sizes.

$$
Q_{2,s}(P_s)=a_2-b_2P_s\\Q_{2,\ell}(P_\ell)=a_2-b_2P_\ell
$$

The choice of which bottle each consumer purchases depends on the prices $P_s$ and $P_\ell$. Consumer 1 will prefer small bottles if $P_s-c_{\text{conv}}<P_\ell$ and vice versa. Consumer 2 looks solely at price, preferring small bottles if $P_s< P_\ell$ and vice versa. The remaining condition we have to ensure is that the demand for consumer 2 is more elastic than consumer 1, representing consumer 2’s higher price sensitivity. This can be done through an appropriate choice of constants.

### Constructing the full model

Now that we have created the equations to model consumption and cost, we can start building our economic model. In this model, we will be individually looking at the demand and supply of small and large bottles for the two types of consumers, for a total of four cases. We shall assume each consumer would choose the bottle size that they consider more valuable, fully consuming only that bottle size, and consuming zero units of the alternative. Additionally, we assume that M&S can perfectly price discriminate towards both consumers’ preferences. We also assume M&S behaves as a monopoly firm, hence being a sole price setter and aiming to maximise profits.

Let us choose some constants for our equations. For our cost functions, we shall choose $c_f=10$, $c_{\text{pack}}=0.02$, $c_{\text{prod}}=0.1$, $d=1$, and $V=1$. This gets us the following cost equations.

$$
C_s(q_s)=0.22q_s\\C_\ell(q_\ell)=0.20q_\ell\\C(q_s, q_\ell)=10+0.22q_s+0.20q_\ell
$$

For consumption, we choose the following constants, $a_1=320$, $b_1=40$, $a_2=500$, $b_2=100$, and $c_{\text{conv}}=0.2$. This gets us the following demand functions.

$$
Q_{1,s}(P_s)=320-40(P_s-0.2)\\Q_{1,\ell}(P_\ell)=320-40P_\ell\\Q_{2,s}(P_s)=500-100P_s\\Q_{2,\ell}(P_\ell)=500-100P_\ell
$$

Let us first consider consumer 2, the consumer that is indifferent to the container size. We shall begin with small bottles first.

Consumer 2 has the demand function of $Q_s=500-100P_s$. The inverse demand function is thus given by $P_s=5-\frac{1}{100}Q_s$. The total revenue is thus given by $\text{TR}_s=P_sQ_s=5Q_s-\frac{1}{100}Q_s^2$, so the marginal revenue is just $\text{MR}_s=\frac{d\text{TR}_s}{dQ_s}=5-\frac{1}{50}Q_s$. We can find the marginal cost with respect to small bottles, by differentiating the cost function with respect to $q_s$. This gives us $\text{MC}_s=\frac{\partial C}{\partial q_s}=0.22$. Notice that we have a constant marginal cost. As this is a monopoly, there is one firm in the market, so $q_s=Q_s$. We can solve for the optimal quantity $Q^*_s$ being produced by setting marginal revenue to equal marginal cost. We get back the optimal price by substituting $Q_s^*$ back into the demand function.

$$
\text{MR}=\text{MC}\\\Rightarrow5-\frac{1}{50}Q_s^*=0.22\\\Rightarrow Q_s^*=239\\\Rightarrow P^*_s=2.61
$$

We see that with the small bottles, the optimal number for M&S to produce is 239 units of smoothie at a price of £2.61 per unit.

With large bottles, the inverse demand function for consumer 2 is the same as for small bottles, hence it is $P_\ell=5-\frac{1}{100}Q_\ell$. The total revenue and marginal revenue are also the same, given as $\text{TR}_\ell=5Q_\ell-\frac{1}{100}Q_\ell^2$, and $\text{MR}_\ell=5-\frac{1}{50}Q_\ell$ respectively. The marginal cost is the derivative of the cost function with respect to $q_\ell$. This is $\text{MC}_\ell=\frac{\partial C}{\partial q_\ell}=0.2$. Notice this is also a constant marginal cost similar to the case with the small bottles.

We solve for the optimal price and quantity in the same way as with the small bottles.

$$
\text{MR}=\text{MC}\\\Rightarrow5-\frac{1}{50}Q_\ell^*=0.2\\\Rightarrow Q_\ell^*=240\\\Rightarrow P^*_\ell=2.60
$$

With the large bottles, M&S would produce 240 units of smoothie at a price of £2.60 per unit. Notice that we have reduced the price as compared to the small bottles, and have ended up selling an extra unit of smoothie.

From the perspective of consumer 2, they would choose large bottles over small bottles as the price per unit of smoothie for large bottles is less than for small bottles, as $P_\ell^*<P_s^*$, since they are indifferent to the container size, .and only consider price.

Let us now consider consumer 1. Similar to before, we shall begin with small bottles. Note that consumer 1 puts value on the convenience of small bottles, and hence is willing to pay a premium for small bottles. The demand function for small bottles is $Q_s=320-40(P_s-0.2)=328-40P_s$. The inverse demand function is given as $P_s=8.2-\frac{1}{40}Q_s$. Similar to before, we can derive the total revenue by multiplying by $Q_s$, and differentiate it to get the marginal revenue. Total revenue is thus $\text{TR}_s=8.2Q_s-\frac{1}{40}Q_s^2$, and marginal revenue is $\text{MR}_s=8.2-\frac{1}{20}Q_s$. The marginal cost is the same as before at $\text{MC}_s=0.22$. Hence, we can solve for the optimal price and quantity.

$$
\text{MR}=\text{MC}\\\Rightarrow8.2-\frac{1}{20}Q_s^*=0.22\\\Rightarrow Q_s^*=159.6\\\Rightarrow P^*_s=4.21
$$

For small bottles, M&S would produce 159.6 units of smoothie at a price of £4.21 per unit. Notice how they can significantly increase the price of small smoothies when selling to consumer 1, as compared to consumer 2. This is the effect of price discrimination.

Now we finish our analysis with large bottles. The demand function for large bottles is $Q_\ell=320-40P_\ell$. This results in an inverse demand function of $P_\ell=8-\frac{1}{40}Q_\ell$. This results in a total revenue of $\text{TR}_\ell=8Q_\ell-\frac{1}{40}Q_\ell^2$ and hence a marginal revenue of $\text{MR}_\ell=8-\frac{1}{20}Q_\ell$. Using the previously found marginal cost of $\text{MC}_\ell=0.2$, we can solve for the optimal price and quantity.

$$
\text{MR}=\text{MC}\\\Rightarrow8-\frac{1}{20}Q_\ell^*=0.2\\\Rightarrow Q_\ell^*=156\\\Rightarrow P^*_\ell=4.10
$$

M&S will choose to produce 156 units of smoothie, selling it at a price of £4.10 per unit. In this case, the price of large bottles of smoothie are still cheaper per unit, but because consumer 1 values convenience, they are willing to pay a premium of £0.20 for small bottles over large bottles. Since $P_s^*-c_{\text{conv}}<P_\ell^*$, consumer 1 would choose small bottles over large bottles.

Given that consumer 1 would purchase small bottles, and consumer 2 would purchase large bottles, we can calculate the total profits made by M&S. To do this, we take the total revenue for each consumer and subtract the total costs of production.

$$
\pi = \text{TR}-\text{TC}\\=240(2.60)+159.6(4.21)-(10+0.2(240)+0.22(159.6))\\=1295.916-93.112\\=1202.804\approx1202.80
$$

With this model, M&S makes a total profit of £1202.80.

### The combined consumption model

To evaluate the effects of price discrimination, we can consider a model with a combined consumption. To do this, we do a horizontal summation of both consumer’s demand functions. The following are the resulting combined demand functions.

$$
Q_s=\begin{cases}828-140P_s&\text{if }0\leq P_s\leq5\\328-40P_s&\text{if }5<P_s\leq8.2\\0&\text{if }P_s>8.2\end{cases}\\Q_\ell=\begin{cases}820-140P_\ell&\text{if }0\leq P_\ell\leq5\\320-40P_\ell&\text{if }5<P_\ell\leq8\\0&\text{if }P_\ell>8\end{cases}
$$

Let us first begin with the case with small bottles. Consider first the equation $Q_s=828-140P_s$. The inverse demand function is thus $P_s=\frac{207}{35}-\frac{1}{140}Q_s$. The marginal revenue for this function is $\text{MR}_s=\frac{207}{25}-\frac{1}{70}Q_s$. The marginal cost is as before at $\text{MC}_s=0.22$. We solve for the optimal price and quantity as before.

$$
\text{MR}=\text{MC}\\\Rightarrow\frac{207}{35}-\frac{1}{140}Q_s^*=0.22\\\Rightarrow Q_s^*=398.6\\\Rightarrow P^*_s=\frac{2147}{700}\approx3.07
$$

In this case, $0\leq P_s^*\leq 5$ so this is an acceptable price and quantity. The other equation we have to consider is $328-40P_s$. Notice how we have done this previously to get $Q^*_s=159.6$ and $P_s^*=4.21$. However, since this does not fall within the range $5<P_s^*\leq 8.2$, this price and quantity is not found on this demand function. Hence, with the first set of values, M&S sells 398.6 units of smoothie in small bottles at a price of £3.07 per unit. Notice how the price now falls between the previous two prices for small bottles of £2.61 and £4.21 when we discriminated to the two consumers.

Lastly, we calculate the profits earned from small bottle sales.

$$
\pi_s = \text{TR}-\text{TC}\\=398.6(\frac{2147}{700})-(10+0.22(398.6))\\=1222.563-97.692\\=1124.871\approx1124.87
$$

M&S earns a total of £1124.87 from the sale of small bottles.

Let us continue with the large bottles case. We first consider the question $Q_\ell=820-140P_\ell$. The inverse demand function is $P_\ell=\frac{41}{7}-\frac{1}{140}Q_\ell$. This results in a marginal revenue of $\text{MR}_\ell=\frac{41}{7}-\frac{1}{70}Q_\ell$. We can solve for the optimal price and quantity as before.

$$
\text{MR}=\text{MC}\\\Rightarrow\frac{41}{7}-\frac{1}{70}Q_\ell^*=0.2\\\Rightarrow Q_\ell^*=396\\\Rightarrow P^*_\ell=\frac{106}{35}\approx3.03
$$

Again, since $0\leq P_\ell^*\leq 5$, this is an acceptable price and quantity. Similar to the small bottles case, we have seen the other question $Q_\ell=320-40P_\ell$, which has the optimal price and quantity of $P^*_\ell=4.10$ and $Q_\ell^*=156$ respectively. However, this price falls outside the range $5<P_\ell^*\leq 8$, and hence is not found on the demand function. With large bottles, M&S would sell 396 units at a price of £3.03 per unit. The total profits from large bottles is given below.

$$
\pi_\ell = \text{TR}-\text{TC}\\=396(\frac{106}{35})-(10+0.2(396))\\=1199.314-89.2\\=1105.114\approx1105.11
$$

M&S earns a total of £1105.11 selling large bottles. Notice that the profits from selling small bottles are larger than selling large bottles, so $\pi_s>\pi_\ell$. Since M&S is profit maximising, and they are able to choose which product to produce for the market, M&S will choose to sell small bottles and earn the higher profit of £1124.87.

Comparing with the previous model using price discrimination, M&S makes a total of £1202.80. This is higher than this combined consumption model which has a profit of £1124.87. By identifying the two types of consumers in the market, M&S can differentiate their products to cater to the different consumers. This allows M&S to sell the smoothie to different consumers at different prices. Price discrimination allows M&S to earn a larger share of the consumer surplus as profits, making M&S better off.

### Concluding discussion

In our hypothetical model, small bottles were priced at £4.21 per unit, while large bottles were priced at £2.60 per unit. As large bottles are 2 units of smoothie each, this comes up to £5.20 per bottle, only £1 more than the price of small bottles. While this is not exactly the same scenario as the cheaper 750ml bottles I had, we can easily see how this may extend that the price of large bottles can become cheaper than the price of small bottles, due to price discrimination.

Now we do have to address some assumptions made. The biggest of which is why would consumers (even the on the go one) purchase the more expensive small bottles when the large bottles are much cheaper. We previously saw that consumer 1 would choose small bottles only if $P_s-c_{\text{conv}}<P_\ell$. In this case, the £4.21 small bottle is much more that £0.20 more than the £2.60 cost of the large bottle per unit of smoothie.

The answer lies in information asymmetry. Normally we like to assume consumers have full information about the goods they can buy. In this case, that might not be so. As mentioned, the small bottles are placed right at the front of the store, while the large bottles are hidden in the back. The consumer that is on the go probably does not have the information about the large bottles, or is unwilling to commit the time to find them. This artificially inflates the demand of small bottles, as large bottles are less substitutable. Consumer 1 might think the only type of smoothie are in the small bottles. On the other hand, consumer 2 looks for the more value for money smoothies, overcoming this information asymmetry and purchasing the larger bottles instead.

An additional assumption we have made is the fact that M&S is a monopoly. We use this idea because M&S has freedom in setting the price of smoothies. In real life, it is much more complex than this, where the price of smoothies are more influenced by market competition. This might be make the problem infeasible to calculate.

Finally, it is obvious that our distinction of two consumers is too simplistic in reality. We have also chosen arbitrary constants to represent the demand functions. However, even with such a simple model, we can identify the two distinct preferences, model the consequences of each consumer having such preferences, and noting how the producer can maximise profits through setting a different price for each consumer.

If you have made it thus far, thank you for being interested enough to finish this. Feel free to check my work, and hopefully you gained as much amusement reading this as I did writing it.