# AI proposed questions
# 1: If a store advertises “up to 50% off,” what share of its items would have to hit 50% before you’d call the ad honest? Who decides that threshold, and why?
# 2: Compared with what? If the “original price” was only ever listed briefly, or was raised shortly before the sale, is a 30% discount still a discount? How would you find out what the price really was before the sale?
# 3: Who bears the cost of the extra charges, and does it matter who collects them? Would your view of “hidden” fees change if a government requires sellers to add them at checkout rather than a seller choosing to add them?
# 4: Do consumers actually behave as if they’re fooled? If shoppers are regularly surprised by the final price, what would you expect to see in cart abandonment, returns, or reviews? And if they’re not surprised, what does that do to your claim?
# 5: Is this about deception or about information? Imagine a market where every seller showed the all-in price upfront. Would the problem you’re describing disappear, shrink, or just move somewhere else (for example, into the discount percentage)?

# Variables for each Question
# Question 1: What share of items must hit 50% before the ad is honest?

Measure: the discount on each item, the share of items at or above 50%, and the share at or above 30%
Choose: how you define “honest” (an actual number, a share of items, or a share of sales volume?)
Distortion: whether the 50% items are popular or obscure, and whether they are in stock
Hold constant: the store, the sale event, and the product category

# Question 2: Compared with what?

Measure: the sale price, the advertised “original” price, and the price history (how long the original was charged, and when it last changed)
Choose: your reference point (the last price, the average price over some window, or a competitor’s price)
Distortion: the time window you pick, since a short window can make nearly any sale look real or fake
Hold constant: the exact product (same model, size, and seller)

# Question 3: Who bears the extra charges, and does the collector matter?

Measure: the advertised price, the final price, and each add-on separately (tax, delivery, service fee, payment fee)
Choose: how you classify each charge (government-imposed or seller-imposed), since your argument depends on that split
Distortion: the location and whether the law requires tax-inclusive pricing
Hold constant: the purchase type (local, online, or cross-border)

# Question 4: Do consumers behave as if they’re fooled?

Measure: cart abandonment rate, return rate, review sentiment, and the stage in checkout where people drop off
Choose: what counts as evidence of surprise (abandonment alone could also mean price comparison)
Distortion: shipping costs and unrelated reasons for leaving a cart
Hold constant: the platform and the period, since sales seasons change behaviour

# Question 5: Deception or information?

Measure: the gap between the advertised and final price, the discount percentage, and how consistently sellers display all-in prices
Choose: what “the problem” is in measurable terms (price gap, consumer trust, or something else)
Distortion: sellers who show all-in prices may differ from the others in other ways, such as size or reputation
Hold constant: the product category and what the buyer is told

# CHECK:
Variables for each question does not exist exist. However price history mentioned in Question 2 can be verified through Date given in the data dictionary.

# Reject
Q3: The dataset only records a single weekly unit price. It contains zero point of sale data, so we there are no variables tracking checkout totals, sales tax, service fees, shipping costs, or seller markups, the dataset cannot tell who collects or bears extra costs. However, most of the time the incidence of the tax falls on the consumer as he might not cancel the purchase even after seeing the additional costs because of embarassement.
Q4: The dataset contains price observations across two cities, it does not track human behavior. It completely lacks variables related to this. Such as, customer review ratings.

# REFLECTION
 The dataset tracks price observations for 4 items across two cities. It measures price trends, calculate weekly price changes and compares average cost differences between two cities for these specific items. This can help us analyze which factors leads to change in price across both cities.However, the dataset cannot verify promotional discount as it lacks original list prices and sale tags. It cannot evaluate hidden taxes or fees. It does not record consumer purchasing behavior, sales volume. Which shows that this data can not measure human behaviour or decision making and motivation and drive behing purchase of a product.

 # LOG ROW
 Field	Entry
Date / time	5 Nov 2026, 01:53-03:34 PKT
Topic	Pricing claims: “up to X% off” and hidden charges
Claims tested	C1: “Up to 50% off” is a ceiling and most items are about 30% off. C2: Final price is much higher than advertised because of hidden taxes and fees.
Coach’s challenges	“Most” and “around 30%” are unmeasured. Is the original price real? “Hidden” vs. shown later at checkout. Taxes and fees are different things.
Questions generated	Q1 honesty threshold for “up to 50%”; Q2 reference price; Q3 who bears the charges; Q4 consumer behavior as evidence of surprise; Q5 deception vs. information
Decisions	Rejected Q3: tests blame and policy, not whether the price gap exists. Rejected Q4: needs platform data I can’t access, and the signals have other explanations. Kept Q1, Q2, Q5.
Variables	Q1: item discount %, share of items at or above 50%. Q2: sale price, claimed original price, price history. Q5: advertised vs. final price, display consistency. Constants: store, event, category.
Open next step	Pick one of Q1/Q2/Q5, name the independent and dependent variable. Note Q4 as out of scope in the write-up.