## Meaningful Names

1. WEBVTT

00:00:00.100 --> 00:00:03.640
D for what days? Data distance.

00:00:04.020 --> 00:00:07.600
If you're guessing, the code has already failed the readability test.

00:00:07.980 --> 00:00:09.180
This single letter

00:00:09.181 --> 00:00:13.561
forces every developer to read the entire code base to understand it.

00:00:13.740 --> 00:00:16.440
That's why your variable names should reveal intent.

00:00:16.820 --> 00:00:19.880
Let's fix your variable names using these proven rules.

00:00:20.660 --> 00:00:23.920
The first rule, use intention revealing names.

00:00:23.980 --> 00:00:26.140
The name should answer why it exists,

00:00:26.141 --> 00:00:28.301
what it does, and how to use it.

00:00:28.302 --> 00:00:30.961
And here's the key, without a single comment.

00:00:31.500 --> 00:00:33.400
Now look at this filtering logic.

00:00:33.660 --> 00:00:36.540
These variables force you to trace back through the code

00:00:36.541 --> 00:00:38.361
to understand what's happening.

00:00:38.660 --> 00:00:40.680
But with intention revealing names,

00:00:40.700 --> 00:00:44.000
you instantly see we're filtering uses by active status.

00:00:44.420 --> 00:00:45.960
Or take this example.

00:00:46.300 --> 00:00:49.720
This calculation uses single letters that hide their meaning.

00:00:49.980 --> 00:00:52.200
You have to guess what each represents.

00:00:52.780 --> 00:00:56.600
The improved version turns a puzzle into a clear pricing formula.

00:00:56.900 --> 00:00:59.980
So remember, you write a variable name once,

00:00:59.981 --> 00:01:03.801
but you and your team will read it hundreds or thousands of times.

00:01:04.180 --> 00:01:06.000
Make those reads effortless.

00:01:06.780 --> 00:01:09.760
Follow for more clean code principles coming next.

2. WEBVTT

00:00:00.220 --> 00:00:02.000
This code is lying to you.

00:00:02.020 --> 00:00:05.280
The word list means something specific to programmers.

00:00:05.340 --> 00:00:07.280
We expect to raise with indexes.

00:00:07.420 --> 00:00:09.160
Yet this is actually a map.

00:00:09.460 --> 00:00:12.240
Clean code demands names that don't mislead.

00:00:12.420 --> 00:00:14.800
So let's fix it using proven patterns,

00:00:14.900 --> 00:00:18.400
making our focus for today avoiding disinformation.

00:00:19.180 --> 00:00:22.160
A variable name should never contain disinformation,

00:00:22.460 --> 00:00:24.800
nor should it promise something it doesn't deliver.

00:00:25.180 --> 00:00:27.840
Trust in code starts with honest naming.

00:00:27.980 --> 00:00:30.560
No surprises, no confusion.

00:00:31.020 --> 00:00:33.080
Let me show you two more examples.

00:00:33.560 --> 00:00:36.880
First, watch out for names varying in small ways.

00:00:37.060 --> 00:00:38.560
Look at these two classes.

00:00:38.700 --> 00:00:40.760
Can you spot the difference instantly?

00:00:41.060 --> 00:00:44.800
You will auto complete the wrong 1/2 the time guaranteed.

00:00:45.340 --> 00:00:48.360
Similarly, another source of disinformation

00:00:48.420 --> 00:00:51.360
comes from using characters that look identical.

00:00:51.900 --> 00:00:54.940
Characters like lowercase L and the No. 1

00:00:54.941 --> 00:00:59.361
or uppercase 0 and zero are visually indistinguishable.

00:00:59.700 --> 00:01:01.580
This creates disinformation

00:01:01.581 --> 00:01:05.441
because the actual code may differ from what developers perceive,

00:01:05.580 --> 00:01:09.080
making the code lie. If it's not a list,

00:01:09.100 --> 00:01:12.520
don't call it a list. If names are similar,

00:01:12.540 --> 00:01:16.040
make them distinct. If characters look identical,

00:01:16.060 --> 00:01:17.640
use better names.

00:01:18.180 --> 00:01:19.240
That's it.

3. WEBVTT

00:00:00.100 --> 00:00:01.740
Without reading the code inside,

00:00:01.741 --> 00:00:05.361
tell me what's the difference between these three functions.

00:00:05.500 --> 00:00:07.860
You can't. And that's the problem.

00:00:07.861 --> 00:00:10.121
Every developer on your team stops,

00:00:10.220 --> 00:00:14.520
reads the implementation, and wastes 5 minutes just to make a choice.

00:00:14.860 --> 00:00:16.780
Clean code has a rule for this.

00:00:16.781 --> 00:00:19.321
Your names must make meaningful distinctions.

00:00:19.820 --> 00:00:23.460
This principle is simple. If two things have different names,

00:00:23.461 --> 00:00:25.201
they must do different things.

00:00:25.260 --> 00:00:29.240
For example, these numbers make every parameter look identical

00:00:29.320 --> 00:00:31.940
even when they do completely different things.

00:00:31.941 --> 00:00:34.881
That's the definition of a meaningless distinction.

00:00:35.260 --> 00:00:38.200
Clear descriptive names solve this instantly

00:00:38.220 --> 00:00:41.040
by revealing each parameter's actual role.

00:00:41.220 --> 00:00:43.160
This applies to classes too.

00:00:43.400 --> 00:00:46.320
If every class is a manager or handler,

00:00:46.460 --> 00:00:48.520
none of them are meaningfully distinct.

00:00:48.660 --> 00:00:50.500
These suffixes are just noise

00:00:50.501 --> 00:00:53.521
that developers add when they can't think of better names.

00:00:53.940 --> 00:00:56.880
Specific role based names on the other hand,

00:00:57.060 --> 00:01:00.480
instantly clarify what each class is responsible for.

00:01:00.740 --> 00:01:04.840
Ultimately, meaningful distinctions eliminate ambiguity

00:01:04.860 --> 00:01:09.320
by ensuring names reflect actual differences in behavior or purpose.

00:01:09.620 --> 00:01:12.000
This makes the code easier to read,

00:01:12.020 --> 00:01:15.720
understand, and safely modify without confusion.

4. WEBVTT

00:00:00.060 --> 00:00:03.920
Try saying this variable name out loud in your next code review.

00:00:04.420 --> 00:00:07.840
If you can't say it, you can't discuss it with your team.

00:00:08.180 --> 00:00:10.480
And it's not just a problem for code reviews.

00:00:10.860 --> 00:00:13.800
This creates a major onboarding bottleneck,

00:00:13.860 --> 00:00:18.200
forcing new hires to decode variables instead of learning the system.

00:00:18.900 --> 00:00:22.160
Clean code has seven suggestions for meaningful names.

00:00:22.500 --> 00:00:26.280
Today's focus use pronounceable names.

00:00:26.620 --> 00:00:28.080
The rule is simple.

00:00:28.140 --> 00:00:31.440
If you can't pronounce a variable name in normal conversation,

00:00:31.460 --> 00:00:36.120
rename it. Your variable names should sound like natural language.

00:00:36.340 --> 00:00:39.720
This is crucial because programming is a social activity.

00:00:40.100 --> 00:00:42.960
This is what unpronounceable code looks like.

00:00:43.180 --> 00:00:44.960
No one can say these names.

00:00:45.620 --> 00:00:49.360
Now, here's the same class with words you can actually speak.

00:00:49.740 --> 00:00:51.720
Suddenly, the code is clear,

00:00:51.820 --> 00:00:56.000
the names are memorable, and your team can actually talk about it.

00:00:56.340 --> 00:00:58.260
Your code is read by humans,

00:00:58.261 --> 00:01:00.601
so make it sound like human language.

00:01:01.060 --> 00:01:03.320
Follow for more clean code principles.

5. WEBVTT

00:00:00.060 --> 00:00:04.320
You see, single letter names and numeric constants have a real problem.

00:00:04.700 --> 00:00:07.720
Basically, they're impossible to locate in a code base.

00:00:08.140 --> 00:00:09.020
Think about it.

00:00:09.021 --> 00:00:13.241
You can search for max classes per student and find it instantly.

00:00:13.620 --> 00:00:15.680
But if you search for the No. 7,

00:00:15.940 --> 00:00:18.460
it appears in file names, other constants,

00:00:18.461 --> 00:00:20.321
and everywhere with different meanings.

00:00:20.780 --> 00:00:23.400
In fact, the letter e is even worse.

00:00:23.620 --> 00:00:27.620
It's the most common letter in English and shows up in every program,

00:00:27.621 --> 00:00:29.921
making searches totally useless.

00:00:30.540 --> 00:00:33.540
Fortunately, clean code has a principle for this.

00:00:33.541 --> 00:00:35.401
Use searchable names.

00:00:35.940 --> 00:00:37.400
The rule is simple.

00:00:37.540 --> 00:00:40.480
The length of a name should match the size of its scope.

00:00:41.100 --> 00:00:43.200
So what about single letters?

00:00:43.700 --> 00:00:45.820
Use them only for local variables.

00:00:45.821 --> 00:00:50.001
In short methods, everything else needs a searchable name.

00:00:50.380 --> 00:00:54.060
For example, look at this calculation here.

00:00:54.061 --> 00:00:56.481
The numbers 4 and 5 could mean anything.

00:00:57.180 --> 00:01:00.040
Now watch the same logic with searchable names.

00:01:00.500 --> 00:01:03.880
Suddenly, you can find work days per week in seconds.

00:01:04.540 --> 00:01:06.420
The code is longer, yes,

00:01:06.421 --> 00:01:09.161
but it becomes infinitely easier to maintain.

00:01:09.820 --> 00:01:13.400
Ultimately, searchable names make your code navigable.

00:01:13.660 --> 00:01:15.920
Follow for more clean code principles.

6. WEBVTT

00:00:00.000 --> 00:00:02.420
Believe it or not, in 1999,

00:00:02.421 --> 00:00:05.321
this naming style was considered best practice.

00:00:05.660 --> 00:00:08.000
But today it's a code smell.

00:00:08.460 --> 00:00:10.760
We call this Hungarian notation.

00:00:10.820 --> 00:00:14.780
And coding the type into every variable name you see.

00:00:14.781 --> 00:00:17.641
Back then, editors couldn't tell you the type.

00:00:17.780 --> 00:00:19.680
You actually had to remember it yourself.

00:00:20.460 --> 00:00:23.960
But here's the thing. Your IDE already knows.

00:00:24.500 --> 00:00:27.040
So really, why encode it twice?

00:00:27.500 --> 00:00:31.000
Clean code calls this principle avoid encodings.

00:00:31.580 --> 00:00:35.120
Just watch modern IDE's show you the type on hover.

00:00:35.380 --> 00:00:38.720
Plus, compilers catch type errors instantly.

00:00:39.020 --> 00:00:42.920
Basically, the encoding solved a problem that no longer exists.

00:00:43.420 --> 00:00:45.760
So go ahead and strip them away.

00:00:45.980 --> 00:00:50.640
Let your tools handle the types and let your names describe the intent.

00:00:51.300 --> 00:00:53.240
Follow to write cleaner code.

7. WEBVTT

00:00:00.000 --> 00:00:03.000
Take a look. This variable stores the hypotheticals,

00:00:03.140 --> 00:00:06.520
but honestly, you'd never know that just by looking at it.

00:00:06.660 --> 00:00:07.660
The problem is

00:00:07.661 --> 00:00:11.241
every cryptic name adds another entry to your mental stack.

00:00:11.420 --> 00:00:14.120
It goes like this. This is the URL.

00:00:14.220 --> 00:00:16.640
This is the user. This is permissions.

00:00:16.820 --> 00:00:19.900
This checks admin status. That's 4 lines,

00:00:19.901 --> 00:00:23.421
4 translations. Your brain becomes a lookup table.

00:00:23.422 --> 00:00:25.241
Instead of focusing on the logic,

00:00:25.580 --> 00:00:28.720
clean code calls this. Avoid mental mapping.

00:00:28.860 --> 00:00:32.400
No one should have to remember what your abbreviations stand for.

00:00:32.539 --> 00:00:34.340
For instance, look at this loop.

00:00:34.341 --> 00:00:36.441
Really? What is it validating?

00:00:36.500 --> 00:00:38.480
You see a t and a t, X.

00:00:38.500 --> 00:00:42.080
But what do they mean? Time, tax, text?

00:00:42.220 --> 00:00:45.120
You actually have to hunt through the code to find out.

00:00:45.160 --> 00:00:47.760
But with real names, there's no mystery.

00:00:47.820 --> 00:00:49.720
We're validating transactions.

00:00:49.900 --> 00:00:52.560
The code tells you exactly what it does.

00:00:52.780 --> 00:00:54.480
Now look at this function.

00:00:54.500 --> 00:00:57.840
What does it calculate? P, t, Q.

00:00:57.940 --> 00:00:59.280
These could mean anything.

00:00:59.420 --> 00:01:02.560
You'd have to trace every call site to understand it.

00:01:02.700 --> 00:01:05.160
Rename them, and suddenly it's obvious.

00:01:05.300 --> 00:01:07.840
Price plus tax times quantity.

00:01:07.900 --> 00:01:10.960
The formula makes sense because the names make sense.

00:01:11.100 --> 00:01:12.820
As Clean Code puts it,

00:01:12.821 --> 00:01:15.641
the professional understands that clarity is king.

00:01:15.860 --> 00:01:19.465
Stop making readers decode your names. Just be clear.

8. WEBVTT

00:00:00.060 --> 00:00:03.120
Reading functions shouldn't feel like a mental workout.

00:00:03.260 --> 00:00:07.440
The problem is long functions bury your logic under layers of noise.

00:00:07.620 --> 00:00:09.580
The more a function tries to do,

00:00:09.581 --> 00:00:12.281
the harder it is to see what's actually happening.

00:00:12.580 --> 00:00:16.520
That's why the first rule of functions is that they should be small.

00:00:16.580 --> 00:00:19.760
The second rule? They should be smaller than that.

00:00:20.100 --> 00:00:22.880
Look at this example. It uploads a file.

00:00:22.980 --> 00:00:27.440
If it's too large, it splits into chunks and uploads piece by piece.

00:00:27.780 --> 00:00:29.960
Otherwise, it uploads directly.

00:00:30.180 --> 00:00:33.480
Let's make it small enough that you don't need me to explain it.

00:00:33.720 --> 00:00:38.240
First, let's wrap these low level details behind clear function names.

00:00:38.700 --> 00:00:40.360
Next, see this loop?

00:00:40.540 --> 00:00:43.380
It's the heaviest part. Let's move it out

00:00:43.381 --> 00:00:45.441
and the complexity moves with it.

00:00:45.540 --> 00:00:49.260
But that's not all. Blocks inside if, else,

00:00:49.261 --> 00:00:50.781
while, and so on.

00:00:50.782 --> 00:00:55.121
Should be one line long. In this case through a function call.

00:00:55.300 --> 00:00:58.660
This achieves two things. Your function stays short,

00:00:58.661 --> 00:01:01.881
and the extracted code gets a name that speaks for itself.

00:01:02.340 --> 00:01:05.140
Now your reader understands what the code does

00:01:05.141 --> 00:01:07.801
without getting bogged down in how it does it,

00:01:07.980 --> 00:01:10.420
and the function no longer demands effort.

00:01:10.421 --> 00:01:12.321
It simply tells a story.

00:01:12.660 --> 00:01:15.680
Follow for more clean code principles coming next.

9. WEBVTT

00:00:00.020 --> 00:00:04.200
A function doing multiple things has multiple reasons to change,

00:00:04.500 --> 00:00:06.120
multiple reasons to break,

00:00:06.580 --> 00:00:08.520
multiple types of tests to write,

00:00:08.780 --> 00:00:12.520
and multiple ways to confuse the next developer who reads it.

00:00:12.540 --> 00:00:14.760
But a function that does one thing,

00:00:15.140 --> 00:00:17.200
it has one reason to change,

00:00:17.420 --> 00:00:21.000
one focused test, one clear purpose.

00:00:21.300 --> 00:00:23.800
It becomes a building block you can trust.

00:00:24.180 --> 00:00:27.080
So how do we know if a function is doing one thing?

00:00:27.580 --> 00:00:29.800
Let me show you two ways to find out.

00:00:29.820 --> 00:00:34.600
First, a function doing one thing cannot be divided into sections.

00:00:34.860 --> 00:00:37.840
If you can label chunks of your code with different names,

00:00:38.060 --> 00:00:40.600
each chunk is a separate responsibility.

00:00:41.180 --> 00:00:44.380
Second, a function is doing more than one thing.

00:00:44.381 --> 00:00:47.581
If you can extract another function from it with a name

00:00:47.582 --> 00:00:50.521
that is not merely a restatement of its implementation.

00:00:51.060 --> 00:00:52.240
Take this function.

00:00:52.460 --> 00:00:55.700
It decides whether to upload a file in multiple parts

00:00:55.701 --> 00:00:58.201
or as a single upload based on size.

00:00:58.580 --> 00:00:59.840
But look here.

00:00:59.940 --> 00:01:04.000
These lines handle the low level details of multipart uploading.

00:01:04.260 --> 00:01:08.200
That's a separate concept we can extract and name meaningfully.

00:01:08.580 --> 00:01:10.800
Now the function reads more clearly.

00:01:10.980 --> 00:01:13.840
It makes a decision and delegates the details.

00:01:14.060 --> 00:01:15.880
But can we extract further?

00:01:16.020 --> 00:01:17.940
If we pull out the remaining logic,

00:01:17.941 --> 00:01:21.281
what would we call it? Upload based on size.

00:01:21.660 --> 00:01:24.740
That's just restating what the code already does.

00:01:24.741 --> 00:01:26.721
The extraction test fails.

00:01:27.100 --> 00:01:30.560
This function is now doing exactly one thing.

00:01:31.020 --> 00:01:34.240
Follow for more clean code principles coming next.

10. WEBVTT

00:00:00.000 --> 00:00:03.520
Functions are the first line of organization in any program.

00:00:03.540 --> 00:00:05.440
And just like any organization,

00:00:05.540 --> 00:00:07.680
they fail when roles get blurred.

00:00:08.020 --> 00:00:12.000
The CEO's function isn't packing boxes or choosing email fonts.

00:00:12.180 --> 00:00:14.280
They operate at the highest level.

00:00:14.620 --> 00:00:16.960
The manager works one step below,

00:00:17.020 --> 00:00:19.600
breaking big goals into smaller ones,

00:00:19.660 --> 00:00:23.760
closer to the details, but still abstracting away the specifics.

00:00:24.220 --> 00:00:28.480
And at the ground level, the specialist handles the real execution.

00:00:28.700 --> 00:00:31.440
Each task focused and distinct.

00:00:32.100 --> 00:00:34.440
Your code needs that same discipline.

00:00:34.740 --> 00:00:37.160
It should read like a top down narrative,

00:00:37.260 --> 00:00:40.240
descending one layer of abstraction at a time.

00:00:40.620 --> 00:00:43.080
Take this function that processes an order.

00:00:43.260 --> 00:00:46.120
It validates stock, calculates the Bill,

00:00:46.220 --> 00:00:49.360
handles payment, and notifies the warehouse.

00:00:49.540 --> 00:00:51.960
But this function is a micromanager.

00:00:52.260 --> 00:00:56.560
Should an order processor really know the raw syntax of Stripe's API?

00:00:57.020 --> 00:01:00.600
Let's delegate. What remains is pure intent.

00:01:00.900 --> 00:01:02.620
The details are still there,

00:01:02.621 --> 00:01:07.481
just not here. Each one handled at its appropriate depth.

00:01:07.740 --> 00:01:09.440
And when you need the details,

00:01:09.620 --> 00:01:10.960
you dive deeper.

00:01:11.540 --> 00:01:14.480
Think of every function as a two paragraph.

00:01:14.740 --> 00:01:17.560
To process an order, we validate stock,

00:01:17.620 --> 00:01:21.920
calculate the Bill, charge the customer and notify the warehouse.

00:01:22.020 --> 00:01:24.640
To calculate the Bill, we sum the items,

00:01:24.740 --> 00:01:27.280
apply discounts, and add tax.

00:01:27.580 --> 00:01:31.280
Each function describes its scope and points to the next.

00:01:31.380 --> 00:01:35.800
Keep every function at its level and the whole system stays clear.

00:01:35.980 --> 00:01:38.920
Follow for more clean code principles coming next.

## Switch Statements

1. WEBVTT

00:00:00.000 --> 00:00:03.680
By their very nature, switch statements do n things.

00:00:03.860 --> 00:00:07.200
That's a problem, because clean functions should do one thing.

00:00:07.540 --> 00:00:11.160
Here we're switching on employee type to calculate pay.

00:00:11.420 --> 00:00:14.100
But we also have to switch on type for benefits,

00:00:14.101 --> 00:00:15.981
for scheduling, for reporting,

00:00:15.982 --> 00:00:19.801
and so on. The same switch copied everywhere.

00:00:20.100 --> 00:00:22.640
Now imagine adding a new employee type.

00:00:22.700 --> 00:00:24.840
You'd have to hunt through every function,

00:00:24.860 --> 00:00:28.320
find every switch and add a new case to each one.

00:00:28.820 --> 00:00:31.240
The solution is to use polymorphism.

00:00:31.380 --> 00:00:34.680
You create an interface that each employee type implements.

00:00:34.980 --> 00:00:37.140
The switch gets buried in a factory.

00:00:37.141 --> 00:00:39.461
It creates the object, nothing more.

00:00:39.462 --> 00:00:41.761
After creation, switches disappear.

00:00:42.020 --> 00:00:45.600
You call the function, and polymorphism handles the dispatch.

00:00:45.860 --> 00:00:48.040
The full time class runs its logic.

00:00:48.060 --> 00:00:50.240
The contractor class runs its own.

00:00:50.300 --> 00:00:52.920
Each object already knows what to do.

00:00:53.180 --> 00:00:54.900
This keeps your functions clean.

00:00:54.901 --> 00:00:57.081
One call, one responsibility.

00:00:57.260 --> 00:01:00.700
The way functions should be follow for more clean code

00:01:00.701 --> 00:01:02.241
principles coming next.

2. WEBVTT

00:00:00.140 --> 00:00:02.680
Look at this, zero arguments.

00:00:03.180 --> 00:00:04.740
There's nothing to remember,

00:00:04.741 --> 00:00:09.161
nothing to mess up. This right here is the ideal function call.

00:00:09.540 --> 00:00:12.440
Add 2 arguments and things change.

00:00:12.540 --> 00:00:14.200
Order starts to matter,

00:00:14.260 --> 00:00:17.280
and your test cases multiply to cover the combinations.

00:00:17.880 --> 00:00:20.680
At 5 arguments, you've entered chaos.

00:00:21.020 --> 00:00:23.560
Test cases explode with every addition,

00:00:23.580 --> 00:00:25.700
and each parameter is one more thing

00:00:25.701 --> 00:00:28.561
developers need to remember when they use your function.

00:00:29.100 --> 00:00:33.360
Why does this matter? Because arguments carry mental weight.

00:00:33.820 --> 00:00:36.060
More arguments lead to more confusion,

00:00:36.061 --> 00:00:39.561
more bugs, and more trips back to the documentation.

00:00:40.100 --> 00:00:43.540
Here's how to fix it. When arguments pile up,

00:00:43.541 --> 00:00:45.521
they're actually telling you something.

00:00:45.540 --> 00:00:47.480
They want to become an object.

00:00:47.900 --> 00:00:49.840
Group the related ones together,

00:00:49.860 --> 00:00:51.380
give that grouping a name

00:00:51.381 --> 00:00:54.201
and pass the idea instead of the pieces.

00:00:54.780 --> 00:00:58.040
So remember, 0 arguments is ideal.

00:00:58.320 --> 00:01:01.520
One is clear, two is acceptable,

00:01:01.540 --> 00:01:05.080
but three, that's your signal to wrap them up.

00:01:05.580 --> 00:01:08.560
Follow for more clean code principles coming next.

3. WEBVTT

00:00:00.100 --> 00:00:02.000
Let's interrogate this function.

00:00:02.060 --> 00:00:03.920
What does this bullion mean?

00:00:04.100 --> 00:00:06.960
True for what? False for what?

00:00:07.180 --> 00:00:09.200
Looking at this call gives us nothing.

00:00:09.340 --> 00:00:11.980
We have to dig through the implementation to understand

00:00:11.981 --> 00:00:13.941
what's happening. Now,

00:00:13.942 --> 00:00:15.961
bullions aren't always the enemy.

00:00:16.220 --> 00:00:18.360
Passing true to set visible,

00:00:18.420 --> 00:00:22.500
that's data. The true is the actual value you need.

00:00:22.501 --> 00:00:25.161
But when it controls which code path runs,

00:00:25.220 --> 00:00:27.820
that's a flag. And flags are a problem

00:00:27.821 --> 00:00:31.921
because they force one function to do two completely different jobs.

00:00:32.400 --> 00:00:34.760
But bullion's aren't our only suspect.

00:00:34.980 --> 00:00:37.880
Output arguments break expectations too.

00:00:38.140 --> 00:00:42.200
Output arguments modify their inputs instead of returning results.

00:00:42.340 --> 00:00:45.440
But we expect data to flow in through arguments

00:00:45.540 --> 00:00:47.760
and out through return values.

00:00:48.060 --> 00:00:50.560
So what does a clean argument look like?

00:00:50.820 --> 00:00:53.800
Single arguments serve three clear purposes.

00:00:53.980 --> 00:00:56.240
A function might be asking a question.

00:00:56.420 --> 00:00:59.360
You pass something in and it gives you an answer back.

00:00:59.580 --> 00:01:02.280
Or a function might be transforming something.

00:01:02.460 --> 00:01:05.760
You pass in an input and it returns something new.

00:01:06.100 --> 00:01:08.400
Or a function might be handling an event.

00:01:08.700 --> 00:01:10.540
Something just happened in your system

00:01:10.541 --> 00:01:12.721
and the function needs to react to it.

00:01:12.860 --> 00:01:15.000
When your arguments follow these patterns,

00:01:15.140 --> 00:01:17.160
your code has nothing to hide.

00:01:17.620 --> 00:01:20.800
Follow for more clean code principles coming next.

4. WEBVTT

00:00:00.000 --> 00:00:02.520
Two arguments aren't always a problem.

00:00:02.700 --> 00:00:04.920
Some pairs, like coordinates,

00:00:05.060 --> 00:00:07.480
act as two halves of one idea.

00:00:07.540 --> 00:00:09.400
They just belong together.

00:00:09.420 --> 00:00:12.560
But usually pairs aren't created equal.

00:00:12.820 --> 00:00:17.080
Here we have two unrelated concepts forced into the same. Cool.

00:00:17.220 --> 00:00:21.040
Which one is first? You have to check every time.

00:00:21.140 --> 00:00:23.800
The fix don't pass them as peers.

00:00:23.980 --> 00:00:25.640
Make one of them the owner.

00:00:25.900 --> 00:00:27.840
Now the relationship is clear.

00:00:28.160 --> 00:00:30.960
Now things get much messier with 3.

00:00:31.020 --> 00:00:33.000
Which one is the expected value?

00:00:33.220 --> 00:00:36.400
They all look valid. Now look at the parameters.

00:00:36.660 --> 00:00:38.280
The message comes first.

00:00:38.580 --> 00:00:42.480
This specific trap catches developers off guard constantly.

00:00:42.820 --> 00:00:45.160
Triads demand extra caution.

00:00:45.260 --> 00:00:48.400
Avoid them where you can, but when you can't.

00:00:48.460 --> 00:00:50.420
Ensure the arguments have a rigid

00:00:50.421 --> 00:00:53.601
natural ordering that readers already expect.

00:00:53.860 --> 00:00:57.040
But sometimes clarity isn't about the count,

00:00:57.180 --> 00:01:00.560
it's about the name. What does this function pass?

00:01:00.780 --> 00:01:02.400
You can't tell from the call.

00:01:02.620 --> 00:01:05.440
Add the noun and now it reads like a sentence.

00:01:05.860 --> 00:01:07.760
The function is the action.

00:01:07.980 --> 00:01:10.440
The argument is the thing it acts on.

00:01:10.620 --> 00:01:13.600
You can even use the name to solve ordering problems.

00:01:13.860 --> 00:01:17.040
Top right, bottom left.

00:01:17.100 --> 00:01:21.360
Encode the order into the name and it becomes its own documentation.

00:01:21.820 --> 00:01:23.700
Your argument should guide readers,

00:01:23.701 --> 00:01:26.561
not confuse them. Make them clear,

00:01:26.660 --> 00:01:29.400
make them obvious, make them readable.

00:01:29.820 --> 00:01:32.760
Follow for more clean code principles coming next.

5. WEBVTT

00:00:00.000 --> 00:00:02.640
On the surface, this makes complete sense.

00:00:02.700 --> 00:00:04.240
If the password matches,

00:00:04.340 --> 00:00:07.200
starting the session feels like the obvious thing to do.

00:00:07.420 --> 00:00:10.060
But the function's name tells a different story.

00:00:10.061 --> 00:00:12.821
It promises to check, nothing more.

00:00:12.822 --> 00:00:15.401
And when code does more than its name promises,

00:00:15.540 --> 00:00:17.720
that's when bugs find their way in.

00:00:18.040 --> 00:00:21.120
What if your user is mid session with items in their cart,

00:00:21.180 --> 00:00:23.400
and they decide to change their password?

00:00:23.900 --> 00:00:27.040
You confirm the current password by calling this function.

00:00:27.060 --> 00:00:31.200
It works, but it also reinitializes the session.

00:00:31.580 --> 00:00:33.440
Suddenly their cart is empty,

00:00:33.460 --> 00:00:37.440
their preferences reset. You just wanted to check something.

00:00:37.540 --> 00:00:39.520
Instead you changed everything.

00:00:40.300 --> 00:00:42.640
Side effects can be even more subtle.

00:00:42.940 --> 00:00:45.760
Here, the function sets a property on the class.

00:00:45.900 --> 00:00:47.880
That's still a hidden change.

00:00:48.260 --> 00:00:52.000
So how do we fix this? One option is to rename it.

00:00:52.020 --> 00:00:55.300
Now the name is honest, but it's also ugly.

00:00:55.301 --> 00:00:57.361
And it still does two things.

00:00:57.620 --> 00:01:01.160
The better approach move the side effect out.

00:01:01.300 --> 00:01:03.100
Let the function do one thing,

00:01:03.101 --> 00:01:06.681
check the password, then handle the session separately.

00:01:07.020 --> 00:01:09.440
Clear name, clear responsibility.

00:01:10.220 --> 00:01:12.480
Side effects make functions lie,

00:01:12.660 --> 00:01:15.800
and lies become bugs. Keep it honest.

00:01:16.540 --> 00:01:19.560
Follow for more clean code principles coming next.

6. WEBVTT

00:00:00.100 --> 00:00:03.660
Look at this condition. We know it sets the attribute value,

00:00:03.661 --> 00:00:05.561
but what is it actually checking?

00:00:06.060 --> 00:00:08.260
Is it checking if the update was successful

00:00:08.261 --> 00:00:10.561
or if the attribute already existed?

00:00:11.020 --> 00:00:14.040
You can't really tell without digging into the implementation,

00:00:14.180 --> 00:00:18.300
and that's a problem. You might try renaming the function to fix it,

00:00:18.301 --> 00:00:21.601
but suddenly the name reveals the real issue.

00:00:21.860 --> 00:00:24.200
This function is doing two jobs.

00:00:24.760 --> 00:00:27.480
It's commanding an action setting the attribute,

00:00:27.660 --> 00:00:29.440
and it's querying the status,

00:00:29.580 --> 00:00:30.840
checking if it existed.

00:00:31.420 --> 00:00:33.320
That's a major code smell

00:00:33.500 --> 00:00:36.320
because it mixes specific actions with questions.

00:00:36.420 --> 00:00:38.320
You can't safely use it.

00:00:38.460 --> 00:00:42.600
Calling it just to check something accidentally changes your data.

00:00:42.780 --> 00:00:44.920
The fix split them up.

00:00:45.020 --> 00:00:47.440
Attribute exists, answers the question.

00:00:47.780 --> 00:00:50.000
Set attribute performs the action.

00:00:50.380 --> 00:00:53.760
Now read the code. It flows like a conversation.

00:00:54.020 --> 00:00:56.020
Does it exist? No.

00:00:56.021 --> 00:00:58.801
Then set it. Commands change state.

00:00:58.860 --> 00:01:02.280
Queries return answers keep them separate.

00:01:02.620 --> 00:01:05.760
Follow for more clean code principles coming next.

7. WEBVTT

00:00:00.000 --> 00:00:02.080
This is how error codes start.

00:00:02.380 --> 00:00:04.800
One operation. 1 check.

00:00:05.300 --> 00:00:07.760
But let me show you where this leads.

00:00:08.060 --> 00:00:10.680
Add a profile, then an email,

00:00:10.820 --> 00:00:13.720
and suddenly you're buried in nested checks.

00:00:14.380 --> 00:00:15.840
That's problem 1.

00:00:15.900 --> 00:00:19.160
But the caller of this function has their own challenge. Now,

00:00:19.420 --> 00:00:21.640
when a function returns an error code,

00:00:21.740 --> 00:00:23.520
the caller can't ignore it.

00:00:23.660 --> 00:00:25.540
They have to handle it right there,

00:00:25.541 --> 00:00:27.841
or the error disappears silently.

00:00:28.080 --> 00:00:31.880
So you end up with another chain of checks at every call site.

00:00:32.260 --> 00:00:33.720
And those error codes,

00:00:33.980 --> 00:00:37.480
they usually live in an enum that every file imports.

00:00:37.860 --> 00:00:41.120
Change it once and you break half your code base.

00:00:41.540 --> 00:00:43.240
So what's the alternative?

00:00:43.540 --> 00:00:48.400
Use try catch instead. Your code now reads like a list of steps.

00:00:48.780 --> 00:00:50.040
No more nesting,

00:00:50.300 --> 00:00:53.360
no more forcing the caller to handle errors immediately.

00:00:53.620 --> 00:00:57.120
And no shared enum tying your code base together.

00:00:57.420 --> 00:01:02.040
But we're not done yet. Try catch blocks confuse the structure.

00:01:02.380 --> 00:01:06.400
Normal processing and error processing are sitting side by side.

00:01:06.620 --> 00:01:09.840
It's better to extract each into its own function.

00:01:10.380 --> 00:01:14.320
Now we have clean separation between logic and error handling.

00:01:14.820 --> 00:01:18.880
That's the principle. Prefer exceptions to returning error codes?

00:01:19.180 --> 00:01:21.420
Your code stays flat, focused,

00:01:21.421 --> 00:01:22.841
and free of clutter.

00:01:23.500 --> 00:01:26.524
Follow for more clean code principles. Coming next.

8. WEBVTT

00:00:00.000 --> 00:00:03.600
Duplication may be the root of all evil in software.

00:00:03.900 --> 00:00:08.640
Think about it. We normalize databases to eliminate redundant data.

00:00:08.940 --> 00:00:13.000
We use inheritance to concentrate shared logic in base classes.

00:00:13.500 --> 00:00:16.720
We build components so we can reuse them everywhere.

00:00:17.140 --> 00:00:21.740
Every innovation since the subroutine has fought the same battle, right?

00:00:21.741 --> 00:00:23.641
Once, not twice.

00:00:24.100 --> 00:00:28.200
Let me show you why. Check out these two API functions.

00:00:28.380 --> 00:00:30.860
They look solid right now.

00:00:30.861 --> 00:00:33.561
Imagine adding a timeout to 20 of them.

00:00:33.780 --> 00:00:35.580
Updating them all is hectic.

00:00:35.581 --> 00:00:39.241
But even worse, if you miss just one,

00:00:39.300 --> 00:00:42.840
you're left with a silent bug waiting to crash your app.

00:00:43.380 --> 00:00:46.240
Here's the solution. Instead of repeating yourself,

00:00:46.460 --> 00:00:50.100
extract it. One function handles fetching,

00:00:50.101 --> 00:00:52.181
error checking, and yes,

00:00:52.182 --> 00:00:55.581
the timeout. Now get users and get posts.

00:00:55.582 --> 00:00:57.481
Just call it with their endpoint.

00:00:57.940 --> 00:00:59.600
Need to change the timeout.

00:00:59.660 --> 00:01:01.560
One place, done.

00:01:01.980 --> 00:01:03.740
This is the dry principle.

00:01:03.741 --> 00:01:07.081
Don't repeat yourself. Or more precisely,

00:01:07.180 --> 00:01:10.860
every piece of knowledge must have a single unambiguous,

00:01:10.861 --> 00:01:14.001
authoritative representation within a system.

00:01:14.500 --> 00:01:16.800
One truth, one place.

00:01:17.100 --> 00:01:20.320
Follow for more clean code principles coming next.

9. WEBVTT

00:00:00.000 --> 00:00:02.120
Functions should be small.

00:00:02.420 --> 00:00:04.480
They should do one thing.

00:00:04.660 --> 00:00:07.720
They should operate at one level of abstraction.

00:00:08.300 --> 00:00:09.920
We've discussed these rules,

00:00:10.220 --> 00:00:14.080
but to be honest, nobody writes clean code on the first try.

00:00:14.500 --> 00:00:16.760
Writing code is like writing an essay.

00:00:17.020 --> 00:00:18.860
We get our thoughts down first.

00:00:18.861 --> 00:00:22.201
Messy and disorganized, nested loops,

00:00:22.260 --> 00:00:25.340
names that mean nothing, long argument lists,

00:00:25.341 --> 00:00:27.721
and duplicated code everywhere.

00:00:28.020 --> 00:00:29.880
And that's completely fine

00:00:30.140 --> 00:00:32.500
as long as we have tests covering all of it.

00:00:32.501 --> 00:00:34.401
We can refactor with confidence.

00:00:34.900 --> 00:00:37.560
We split functions, find better names,

00:00:37.620 --> 00:00:41.400
eliminate duplication, iteration by iteration,

00:00:41.420 --> 00:00:43.920
the code starts following every rule.

00:00:44.300 --> 00:00:46.120
So clean code isn't written,

00:00:46.140 --> 00:00:47.360
it's rewritten.

00:00:47.900 --> 00:00:50.920
Follow for more clean code principles, coming next.

## Commenting

Intro. WEBVTT

00:00:00.000 --> 00:00:02.500
Comments lie. Not intentionally,

00:00:02.501 --> 00:00:07.521
but they do. Here's how code changes and evolves.

00:00:07.740 --> 00:00:09.780
It moves, it splits,

00:00:09.781 --> 00:00:12.041
it merges. But comments?

00:00:12.340 --> 00:00:13.800
They get left behind,

00:00:13.860 --> 00:00:17.360
still telling the old story while the code writes a new one.

00:00:17.660 --> 00:00:20.960
An inaccurate comment is worse than no comment at all.

00:00:21.220 --> 00:00:22.940
It doesn't just fail to help,

00:00:22.941 --> 00:00:27.161
it actively deceives. So should you never write comments?

00:00:27.620 --> 00:00:31.880
No, but you need to know which ones help and which ones hurt.

00:00:32.180 --> 00:00:33.840
That's what's coming next.

00:00:34.100 --> 00:00:37.000
Follow for the clean code principles coming next.

1. WEBVTT

00:00:00.000 --> 00:00:02.000
The best code needs no comments.

00:00:02.340 --> 00:00:03.300
But sometimes

00:00:03.301 --> 00:00:06.081
there are things your code will never be able to tell you.

00:00:06.380 --> 00:00:07.920
Take this logic here

00:00:07.980 --> 00:00:10.980
A new developer might see this limit as a bottleneck

00:00:10.981 --> 00:00:13.681
and try to optimize it away.

00:00:14.020 --> 00:00:15.460
The comment prevents that,

00:00:15.461 --> 00:00:18.261
explaining it's actually a strict business decision

00:00:18.262 --> 00:00:20.361
that keeps the free tier viable.

00:00:20.820 --> 00:00:23.440
Sometimes comments save mental energy.

00:00:23.580 --> 00:00:27.480
Look at this pattern. Instead of forcing us to decipher the symbols,

00:00:27.580 --> 00:00:29.680
the comment acts as a translator,

00:00:29.700 --> 00:00:31.880
giving us the rules in plain English.

00:00:32.259 --> 00:00:34.180
And finally, they can decode.

00:00:34.181 --> 00:00:38.001
The complex compared to returns are non intuitive,

00:00:38.060 --> 00:00:41.120
and we often forget what the numbers actually represent.

00:00:41.380 --> 00:00:42.620
The comment fixes this

00:00:42.621 --> 00:00:45.841
by simply translating the math into a readable statement.

00:00:46.100 --> 00:00:48.880
But remember, accuracy is everything.

00:00:49.380 --> 00:00:52.180
If your comment claims A is less than B,

00:00:52.181 --> 00:00:54.261
but the logic proves they are equal,

00:00:54.262 --> 00:00:55.821
you aren't helping the reader.

00:00:55.822 --> 00:00:58.781
You're setting a trap. So if you write them,

00:00:58.782 --> 00:01:00.721
you must maintain them.

00:01:01.060 --> 00:01:04.040
Follow for more clean code principles coming next.

2. WEBVTT

00:00:00.000 --> 00:00:02.760
Some comments aren't just about explaining code,

00:00:02.980 --> 00:00:05.960
they're about protecting the people who come after you.

00:00:06.180 --> 00:00:08.760
The most direct way to do that is a warning.

00:00:09.060 --> 00:00:10.600
Look at this test function.

00:00:10.860 --> 00:00:14.840
The name is generic, but the comment makes it clear that this is slow.

00:00:14.940 --> 00:00:17.640
It warns you to skip it during quick cycles.

00:00:18.020 --> 00:00:22.460
Or take this date format. A developer might look at this and think

00:00:22.461 --> 00:00:25.041
why not optimize this into a shared instance?

00:00:25.340 --> 00:00:26.820
The comment stops them

00:00:26.821 --> 00:00:30.201
explaining that optimization causes concurrency bugs.

00:00:30.420 --> 00:00:33.280
It prevents a cleanup from breaking production.

00:00:33.700 --> 00:00:36.700
Then there's amplification comments that say

00:00:36.701 --> 00:00:39.621
this matters more than it looks here

00:00:39.622 --> 00:00:41.481
the code sets an expiry date.

00:00:41.620 --> 00:00:46.560
That plus 1 looks random, but the comment clarifies the Y immediately.

00:00:46.820 --> 00:00:50.700
It tells us the extra day is needed for users west of UTC

00:00:50.701 --> 00:00:54.561
to prevent early expiry. Finally we have to do's.

00:00:54.940 --> 00:00:58.360
These are for work that should be done but can't happen yet,

00:00:58.420 --> 00:01:00.520
like this Chrome bug workaround.

00:01:00.700 --> 00:01:03.120
The fix is out of your hands for now.

00:01:03.180 --> 00:01:06.860
That's a valid to do. Just make sure you're tracking a reason,

00:01:06.861 --> 00:01:08.801
not just delaying clean code.

00:01:09.100 --> 00:01:13.200
Good code works today, good comments ensure it works tomorrow.

00:01:13.660 --> 00:01:16.632
Follow for more clean code principles coming next.

3. WEBVTT

00:00:00.020 --> 00:00:02.320
Code actually has two audiences

00:00:02.460 --> 00:00:04.420
your team who reads the code,

00:00:04.421 --> 00:00:07.001
and the world who reads the documentation.

00:00:07.380 --> 00:00:09.420
When internal code is written well,

00:00:09.421 --> 00:00:13.001
it rarely needs comments. But for external users,

00:00:13.060 --> 00:00:15.100
documentation lets them understand it

00:00:15.101 --> 00:00:17.521
without having to read the implementation.

00:00:17.920 --> 00:00:21.320
Good docs follow a simple pattern what it does,

00:00:21.380 --> 00:00:23.900
what goes in, what comes out,

00:00:23.901 --> 00:00:27.041
what can go wrong, and a usage example.

00:00:27.300 --> 00:00:30.940
This gives developers everything they need to use your code correctly

00:00:30.941 --> 00:00:32.740
the first time. But

00:00:32.741 --> 00:00:35.581
documentation is only one part of getting your library

00:00:35.582 --> 00:00:38.801
ready for the public. The other part is compliance.

00:00:39.140 --> 00:00:41.700
So when copyrights and licenses are required,

00:00:41.701 --> 00:00:45.561
refer to a standard license instead of writing a full contract.

00:00:45.980 --> 00:00:47.460
Keep them at the top of the file

00:00:47.461 --> 00:00:50.281
where modern IDE's collapse them automatically

00:00:50.460 --> 00:00:52.520
so they stay out of your way.

00:00:52.820 --> 00:00:55.980
With proper documentation and legal headers in place,

00:00:55.981 --> 00:00:58.401
your code is finally ready for the world.

00:00:58.820 --> 00:01:02.480
Follow for more clean code principles coming next.

4. WEBVTT

00:00:00.000 --> 00:00:01.700
If there are no items in the cart,

00:00:01.701 --> 00:00:06.561
return early. The comment communicated nothing the code hadn't already.

00:00:06.820 --> 00:00:08.480
That's a redundant comment,

00:00:08.620 --> 00:00:12.040
a comment that restates what the code already says.

00:00:12.580 --> 00:00:15.160
It adds words not understanding.

00:00:15.820 --> 00:00:18.840
Similarly, noise comments offer nothing of value.

00:00:18.980 --> 00:00:22.120
They restate the obvious, offer no new information,

00:00:22.220 --> 00:00:24.620
and exist as labels over your code

00:00:24.621 --> 00:00:27.201
that repeat what the names already tell you.

00:00:27.500 --> 00:00:30.200
And sometimes this clutter is forced on you.

00:00:30.340 --> 00:00:34.040
Some teams have a rule that every function must have a DOC comment,

00:00:34.420 --> 00:00:38.640
so developers write comments that exist only to satisfy that rule.

00:00:39.060 --> 00:00:40.660
This clutter adds nothing

00:00:40.661 --> 00:00:43.181
and serves only to obfuscate the code

00:00:43.182 --> 00:00:46.441
and create the potential for lies and misdirection.

00:00:46.980 --> 00:00:49.400
Now here are the actual consequences.

00:00:49.980 --> 00:00:51.760
First, it creates clutter.

00:00:52.100 --> 00:00:56.080
You double the lines you have to scan without adding any understanding.

00:00:56.660 --> 00:00:58.200
Second, it's maintenance.

00:00:58.380 --> 00:01:00.180
Every time you change the code,

00:01:00.181 --> 00:01:04.401
you have to update a useless comment or risk it becoming a lie.

00:01:04.740 --> 00:01:07.120
And third, it creates blindness.

00:01:07.460 --> 00:01:09.480
When comments say nothing new,

00:01:09.500 --> 00:01:12.000
developers learn to skip all of them.

00:01:12.300 --> 00:01:15.560
So when you finally write a comment that actually matters,

00:01:16.220 --> 00:01:20.080
nobody reads it. So the solution is simple

00:01:20.460 --> 00:01:22.160
respect your reader's time.

00:01:22.300 --> 00:01:25.920
They can read the code. Only interrupt them with a comment

00:01:25.940 --> 00:01:29.560
when you have something to say that the code can't say for you.

00:01:30.100 --> 00:01:33.200
Follow for more clean code principles coming next.

5. WEBVTT

00:00:00.000 --> 00:00:02.720
A comment doesn't have to be a lie to be dangerous.

00:00:03.100 --> 00:00:06.900
Sometimes the worst comments are the ones that are technically true

00:00:06.901 --> 00:00:11.121
but practically useless. Here is exactly what I mean.

00:00:11.460 --> 00:00:12.540
Take this function.

00:00:12.541 --> 00:00:16.041
The comment tells us it returns the discount for premium users,

00:00:16.260 --> 00:00:19.520
and sure enough, premium users get 20%.

00:00:19.860 --> 00:00:22.280
But if you actually read the implementation,

00:00:22.500 --> 00:00:25.080
non premium users get a discount too.

00:00:25.340 --> 00:00:28.440
The comment gives you false confidence to stop reading.

00:00:28.540 --> 00:00:32.160
And a misleading comment is worse than no comment at all.

00:00:32.439 --> 00:00:35.800
Then there are comments that raise more questions than answers.

00:00:36.100 --> 00:00:40.000
Take this calculation. It says allow room for the header and padding.

00:00:40.340 --> 00:00:42.800
Okay, but which part is the header?

00:00:42.940 --> 00:00:46.760
Is it the times 4? The plus 12? Both?

00:00:47.140 --> 00:00:49.980
The whole purpose of a comment is to explain code

00:00:49.981 --> 00:00:51.761
that doesn't explain itself.

00:00:52.260 --> 00:00:54.520
If this code needs the help of a comment,

00:00:54.580 --> 00:00:57.480
but the comment needs its own comment to be understood,

00:00:57.820 --> 00:01:00.040
that's a pity. Finally,

00:01:00.180 --> 00:01:03.280
never write a comment about code you don't control.

00:01:03.660 --> 00:01:08.200
Look at this setter. The comment claims a default of 5,000 milliseconds,

00:01:08.580 --> 00:01:11.200
but this function doesn't decide that default.

00:01:11.580 --> 00:01:14.440
The default is decided somewhere else entirely.

00:01:14.900 --> 00:01:17.600
When someone changes that default in the other file,

00:01:17.700 --> 00:01:19.480
they'll never find this comment.

00:01:19.940 --> 00:01:23.800
If you write a comment, keep it about the code right next to it.

00:01:24.100 --> 00:01:26.980
So the rules are simple be specific,

00:01:26.981 --> 00:01:29.281
be obvious, and stay local.

00:01:29.540 --> 00:01:32.880
If a comment forces the reader to guess or go hunting,

00:01:33.020 --> 00:01:35.280
it's not helping. It's hurting.

00:01:35.780 --> 00:01:38.960
Follow for more clean code principles coming next.

6. WEBVTT

00:00:00.060 --> 00:00:03.440
Don't delete that code. What if we need it again?

00:00:03.940 --> 00:00:07.820
So you comment it out. It starts with one function here,

00:00:07.821 --> 00:00:11.641
a few lines there, maybe an entire block somewhere else.

00:00:11.660 --> 00:00:14.220
But now your file is half alive,

00:00:14.221 --> 00:00:17.321
half dead, like artifacts in a museum.

00:00:17.740 --> 00:00:19.580
So stop keeping it around.

00:00:19.581 --> 00:00:21.481
Delete the commented code,

00:00:21.620 --> 00:00:24.180
all of it. If you need it back.

00:00:24.181 --> 00:00:27.281
Your version control has every line you've ever written.

00:00:27.820 --> 00:00:31.040
This also means you don't need attributions in your code.

00:00:31.380 --> 00:00:34.080
Having the author's name at the top seems useful

00:00:34.300 --> 00:00:37.160
if you have a question. You know who to talk to.

00:00:37.380 --> 00:00:40.160
But over time, other people make changes,

00:00:40.260 --> 00:00:43.440
the file evolves, and that name at the top,

00:00:43.660 --> 00:00:47.840
it stays there forever, long after it stopped being relevant.

00:00:48.300 --> 00:00:50.320
The same goes for journal comments,

00:00:50.460 --> 00:00:52.640
those dated logs of every edit.

00:00:53.080 --> 00:00:55.680
Your version control already does that too,

00:00:55.700 --> 00:00:58.040
better than any comment ever could.

00:00:58.380 --> 00:01:01.160
So please leave the history to get.

00:01:01.740 --> 00:01:04.760
Your code should only contain what runs today.

00:01:04.900 --> 00:01:07.520
Everything else is already in your history.

00:01:08.060 --> 00:01:11.040
Follow for more clean code principles coming next.

7. WEBVTT

00:00:00.000 --> 00:00:03.000
Some comments are apologies for poor code structure.

00:00:03.180 --> 00:00:06.460
They attempt to compensate for code that has become too large,

00:00:06.461 --> 00:00:09.601
too complex, or lacks proper modularity.

00:00:09.860 --> 00:00:11.700
For example, closing brace

00:00:11.701 --> 00:00:15.361
comments appear when a function gets so long or deeply nested

00:00:15.620 --> 00:00:18.120
that you can no longer see where a block ends.

00:00:18.460 --> 00:00:22.000
Sure, they help you track which brace closes which block,

00:00:22.100 --> 00:00:25.100
but these comments are symptoms of the problem,

00:00:25.101 --> 00:00:26.441
not the solution.

00:00:27.020 --> 00:00:30.640
The solution is to write clean functions that do one thing.

00:00:30.700 --> 00:00:34.560
Do that, and you'll never need a comment to tell you where a block ends.

00:00:35.260 --> 00:00:37.520
The same applies for position markers.

00:00:37.820 --> 00:00:41.720
These separators try to organize a file that's doing too much

00:00:41.980 --> 00:00:45.380
authentication here, database queries there,

00:00:45.381 --> 00:00:46.921
file handling below.

00:00:47.060 --> 00:00:50.880
But drawing lines between sections doesn't reduce complexity,

00:00:50.980 --> 00:00:53.120
it just makes the mess look tidy.

00:00:53.500 --> 00:00:57.640
Now, there are rare cases where a position marker might be acceptable.

00:00:57.860 --> 00:01:00.940
For example, if a framework requires boilerplate

00:01:00.941 --> 00:01:03.681
that naturally splits into distinct groups,

00:01:03.780 --> 00:01:07.760
a marker can help, but only when the benefit is clear.

00:01:07.980 --> 00:01:11.960
Overuse them and they become the very noise you're trying to fix.

00:01:12.620 --> 00:01:16.280
So remember, if your comments are apologizing for the code,

00:01:16.460 --> 00:01:19.360
the code needs to change, not the comments.

00:01:19.700 --> 00:01:21.920
Clean structure speaks for itself.

00:01:22.420 --> 00:01:25.600
Follow for more clean code principles coming next.

8. WEBVTT

00:00:00.140 --> 00:00:04.560
Some comments technically exist but completely fail at communicating.

00:00:04.860 --> 00:00:05.820
They mumble,

00:00:05.821 --> 00:00:09.801
dump irrelevant details or become unreadable in your editor.

00:00:10.180 --> 00:00:12.240
For example, look at this comment.

00:00:12.500 --> 00:00:18.840
Who is RJ? Which edge case and what does not sure if it works even mean?

00:00:19.180 --> 00:00:21.960
If you're unsure, don't mumble about it.

00:00:22.140 --> 00:00:25.520
Write a clear to do that explains the actual constraint.

00:00:25.820 --> 00:00:29.720
Now the next developer knows exactly what's wrong and what to look for.

00:00:29.980 --> 00:00:32.940
But sometimes the problem isn't saying too little,

00:00:32.941 --> 00:00:35.121
it's saying way too much.

00:00:35.380 --> 00:00:38.760
This comment is basically a novel for a one line function.

00:00:39.140 --> 00:00:42.220
Dave from 2018, an RFC number,

00:00:42.221 --> 00:00:44.641
a library bug from a dead dependency.

00:00:44.780 --> 00:00:48.760
This comment is a history lesson and none of that helps you today.

00:00:48.900 --> 00:00:50.200
Just delete it.

00:00:50.300 --> 00:00:54.240
The code already tells you what it does without any need for a comment.

00:00:54.700 --> 00:00:57.200
And finally, there's the issue of formatting,

00:00:57.260 --> 00:00:59.960
specifically using HTML tags.

00:01:00.340 --> 00:01:02.460
When rendered on a documentation site,

00:01:02.461 --> 00:01:04.081
these comments look beautiful,

00:01:04.300 --> 00:01:09.200
but in your editor, your eyes filter through tags just to read English.

00:01:09.380 --> 00:01:11.100
And if you need to change a word,

00:01:11.101 --> 00:01:13.921
you're editing around tags instead of text.

00:01:14.460 --> 00:01:19.120
The fix is simple. Use plain text which is readable everywhere.

00:01:19.620 --> 00:01:22.020
A good comment is clear, relevant,

00:01:22.021 --> 00:01:24.921
and readable exactly where you write code.

00:01:25.100 --> 00:01:26.800
Anything else is noise.

00:01:27.220 --> 00:01:30.240
Follow for more clean code principles coming next.

## Formatting

1. WEBVTT

00:00:00.000 --> 00:00:02.440
Your source file should read like a newspaper.

00:00:02.660 --> 00:00:04.620
The headline tells you what happened,

00:00:04.621 --> 00:00:08.401
and in your code, that headline is your highest level function.

00:00:08.780 --> 00:00:12.360
Place it at the top of your file in three lines.

00:00:12.380 --> 00:00:15.000
Any developer knows what this code does.

00:00:15.220 --> 00:00:17.300
Fetch data, build a report,

00:00:17.301 --> 00:00:19.601
save it. That's your headline.

00:00:20.060 --> 00:00:21.640
And just like a newspaper,

00:00:21.660 --> 00:00:24.960
the next detail should sit right below where it's mentioned.

00:00:25.340 --> 00:00:28.220
Place every function just below its caller

00:00:28.221 --> 00:00:31.121
so the code reads in a natural downward flow

00:00:31.220 --> 00:00:34.600
from high level concepts down to low level details.

00:00:35.020 --> 00:00:37.120
Look at how Fetch User Data,

00:00:37.260 --> 00:00:38.380
Build Report,

00:00:38.381 --> 00:00:42.321
and Save Report are defined in the same order they were called.

00:00:42.500 --> 00:00:44.960
This builds trust with every reader.

00:00:45.300 --> 00:00:46.940
When they see a function call,

00:00:46.941 --> 00:00:49.801
they know its definition is coming right below.

00:00:50.340 --> 00:00:53.080
But there's another reason to keep functions close.

00:00:53.380 --> 00:00:55.060
Not because one calls the other,

00:00:55.061 --> 00:00:57.561
but because they serve a similar purpose.

00:00:58.020 --> 00:01:00.800
Look at format date and format score.

00:01:01.100 --> 00:01:04.360
They both format values and share a naming pattern.

00:01:04.820 --> 00:01:07.640
Clean code calls this conceptual affinity.

00:01:07.980 --> 00:01:12.000
Group them together and your file naturally organizes into layers.

00:01:12.500 --> 00:01:14.280
The big picture at the top,

00:01:14.380 --> 00:01:17.600
supporting functions flowing downward in call order,

00:01:17.820 --> 00:01:21.280
and shared utilities grouped by purpose at the bottom.

00:01:21.940 --> 00:01:24.480
That's how your code reads like a newspaper.

00:01:24.780 --> 00:01:27.920
Follow for more clean code principles coming next.

2. WEBVTT

00:00:00.000 --> 00:00:01.600
This is a well written code.

00:00:01.740 --> 00:00:05.040
The names reveal intent, the methods are focused.

00:00:05.500 --> 00:00:07.280
Yet it's still hard to read.

00:00:07.340 --> 00:00:09.920
All because there's no vertical spacing.

00:00:09.940 --> 00:00:11.740
As soon as we add that spacing,

00:00:11.741 --> 00:00:14.861
every blank line tells you new concept starts.

00:00:14.862 --> 00:00:18.361
Here you scan instead of reading every line.

00:00:18.580 --> 00:00:20.800
Navigate to any section in a glance.

00:00:21.060 --> 00:00:24.460
The mental effort drops because your brain processes groups

00:00:24.461 --> 00:00:26.721
far more easily than a wall of text.

00:00:26.860 --> 00:00:28.920
But spacing works both ways.

00:00:29.060 --> 00:00:31.280
If blank lines separate concepts,

00:00:31.300 --> 00:00:34.120
then related lines should stay vertically dense.

00:00:34.380 --> 00:00:39.080
Take this block of code. Spacing everywhere disconnects related code.

00:00:39.220 --> 00:00:42.120
Spacing nowhere makes it all look the same.

00:00:42.140 --> 00:00:44.440
Both are equally hard to scan.

00:00:44.860 --> 00:00:47.840
Instead, let density show what belongs together.

00:00:48.020 --> 00:00:49.840
Data extraction at the top,

00:00:49.860 --> 00:00:51.460
business logic in the middle,

00:00:51.461 --> 00:00:53.121
and the result at the end.

00:00:53.260 --> 00:00:57.000
Three distinct groups, each with a single clear purpose.

00:00:57.220 --> 00:01:00.220
With our blocks defined, there's just one more layer of structure.

00:01:00.221 --> 00:01:02.601
To add proper indentation,

00:01:02.840 --> 00:01:05.400
where each scope level gets its own indent,

00:01:05.420 --> 00:01:07.940
and your code becomes a visual hierarchy.

00:01:07.941 --> 00:01:09.841
You can navigate at a glance.

00:01:10.140 --> 00:01:13.480
Good formatting means your code speaks before it's read.

00:01:13.700 --> 00:01:16.840
Follow for more clean code principles coming next.

3. WEBVTT

00:00:00.020 --> 00:00:02.020
Every variable declared too early

00:00:02.021 --> 00:00:05.401
is baggage your brain carries until it's finally used.

00:00:05.900 --> 00:00:09.600
For example, these two variables are declared right at the top,

00:00:09.620 --> 00:00:13.100
but skipped log is only used inside a nested block,

00:00:13.101 --> 00:00:16.041
and report isn't needed until the last few lines.

00:00:16.620 --> 00:00:17.980
When reading this code,

00:00:17.981 --> 00:00:21.761
we carry these variables in our mental stack throughout the function

00:00:21.820 --> 00:00:24.200
just to use them in two small places.

00:00:24.700 --> 00:00:26.840
So why not just move them there?

00:00:27.220 --> 00:00:29.680
Skipped log moves inside its block,

00:00:29.700 --> 00:00:32.200
and report moves right where it's used.

00:00:32.540 --> 00:00:35.600
Now you only encounter a variable when you need it.

00:00:36.100 --> 00:00:38.160
If this works for local variables,

00:00:38.180 --> 00:00:40.560
should it work for class properties too?

00:00:40.940 --> 00:00:41.860
For example,

00:00:41.861 --> 00:00:45.441
this validator is declared right above the function where it's used.

00:00:45.620 --> 00:00:49.520
Seems logical, but it's a class property for a reason.

00:00:49.660 --> 00:00:52.720
Most likely because other functions rely on it too.

00:00:52.780 --> 00:00:57.840
And sure enough, export uses uses the same validator right here.

00:00:58.100 --> 00:01:00.920
By design, class properties are shared.

00:01:00.980 --> 00:01:04.220
Placing them near one function only makes them harder to find.

00:01:04.221 --> 00:01:05.121
For the rest,

00:01:05.700 --> 00:01:08.720
instead, keep them in one designated place.

00:01:09.020 --> 00:01:10.940
Some languages place them at the bottom,

00:01:10.941 --> 00:01:13.361
but most prefer the top of the class.

00:01:13.540 --> 00:01:16.880
What matters is which standard the team decides to follow,

00:01:17.220 --> 00:01:19.080
and this applies to everything.

00:01:19.500 --> 00:01:22.320
Do your braces go on the same line or the next?

00:01:22.540 --> 00:01:27.200
Are these tabs or spaces? Does the team use single quotes or double?

00:01:27.300 --> 00:01:30.540
These are team decisions. The result is a code base

00:01:30.541 --> 00:01:34.341
where formatting never gets in the Way of understanding follow

00:01:34.342 --> 00:01:36.961
for more clean code principles coming next.

## Objects and Data

1. WEBVTT

00:00:00.000 --> 00:00:02.180
Most developers make their variables private,

00:00:02.181 --> 00:00:05.181
then immediately add getters and setters for every one of them,

00:00:05.182 --> 00:00:07.561
which effectively makes them public again.

00:00:07.820 --> 00:00:10.020
The whole reason to keep variables private

00:00:10.021 --> 00:00:12.141
is the freedom to change how they're stored

00:00:12.142 --> 00:00:13.641
without breaking dependence.

00:00:13.940 --> 00:00:17.840
That freedom disappears the moment you expose the shape of the data.

00:00:18.260 --> 00:00:21.560
Hiding implementation isn't about adding a layer of functions.

00:00:21.660 --> 00:00:26.340
It's about abstraction. This class stores a point as x and y,

00:00:26.341 --> 00:00:27.841
rectangular coordinates.

00:00:28.140 --> 00:00:31.260
This one stores the same point as radius and theta,

00:00:31.261 --> 00:00:34.601
polar coordinates. Same point on the same plane.

00:00:34.620 --> 00:00:36.920
Two completely different representations,

00:00:37.260 --> 00:00:40.280
but both classes expose the implementation,

00:00:40.340 --> 00:00:44.140
not the functionality. Abstract the implementation away,

00:00:44.141 --> 00:00:47.441
and you can still get X and y or radius and theta,

00:00:47.860 --> 00:00:49.880
set Cartesian or polar.

00:00:50.140 --> 00:00:53.640
The caller manipulates the data without ever knowing how it's stored,

00:00:53.860 --> 00:00:55.680
and it does one more thing.

00:00:55.700 --> 00:00:58.400
The interface can set an access policy.

00:00:58.780 --> 00:01:00.980
You can read coordinates independently,

00:01:00.981 --> 00:01:04.281
but you must set them together as an atomic operation.

00:01:04.540 --> 00:01:07.320
Public fields have no way to enforce that.

00:01:07.600 --> 00:01:10.380
Abstraction is not just about hiding fields.

00:01:10.381 --> 00:01:13.401
It's about exposing behaviour rather than structure.

00:01:13.740 --> 00:01:16.000
Take this interface that a vehicle uses.

00:01:16.180 --> 00:01:20.200
The fields are hidden, but the methods still describe just the fields.

00:01:20.580 --> 00:01:24.400
On the other hand, this interface only exposes behavior.

00:01:24.420 --> 00:01:28.840
Percent fuel remaining. We have no clue about the form of the data.

00:01:28.900 --> 00:01:30.840
Is it in gallons, liters?

00:01:30.940 --> 00:01:32.760
Is it diesel electric?

00:01:33.020 --> 00:01:36.960
None of that matters. The implementation is genuinely gone.

00:01:37.460 --> 00:01:41.120
Serious thought needs To go into how you represent an object's data,

00:01:41.420 --> 00:01:45.200
the worst thing you can do is blindly add getters and setters.

00:01:45.380 --> 00:01:47.900
Expose what users can do with the data,

00:01:47.901 --> 00:01:49.801
not how the data is stored.

00:01:50.220 --> 00:01:53.280
Follow for more clean code principles coming next.

2. WEBVTT

00:00:00.000 --> 00:00:02.160
Every class you write is a bet.

00:00:02.340 --> 00:00:05.200
A bet on what kind of change comes next.

00:00:05.700 --> 00:00:08.020
Consider three shapes. Square,

00:00:08.021 --> 00:00:09.921
rectangle, and circle.

00:00:10.260 --> 00:00:13.160
They're just data. No behavior at all.

00:00:13.580 --> 00:00:16.560
All the behavior lives in a separate geometry class

00:00:16.580 --> 00:00:19.560
that takes any shape and calculates its area.

00:00:20.300 --> 00:00:22.920
So what happens when we need a perimeter function?

00:00:23.220 --> 00:00:25.840
We add it to geometry, and that's it.

00:00:26.260 --> 00:00:27.960
The shapes don't change.

00:00:27.980 --> 00:00:30.560
And nothing that depends on them changes either.

00:00:31.300 --> 00:00:33.720
But what happens when we add a new shape?

00:00:34.260 --> 00:00:39.380
Now, every function in geometry needs a new case, area, perimeter,

00:00:39.381 --> 00:00:40.481
all of them.

00:00:41.100 --> 00:00:44.240
That's the cost of keeping behavior separate from data.

00:00:44.860 --> 00:00:46.960
So what if we took the opposite approach?

00:00:47.380 --> 00:00:49.340
Same shapes, but this time,

00:00:49.341 --> 00:00:51.361
each one owns its behavior.

00:00:51.700 --> 00:00:53.800
There's no geometry class needed.

00:00:54.340 --> 00:00:56.440
Now, adding a new shape is simple.

00:00:56.540 --> 00:00:59.240
One new class. Nothing else changes.

00:01:00.180 --> 00:01:01.940
But adding a perimeter function

00:01:01.941 --> 00:01:04.681
means every shape class needs a new method.

00:01:05.060 --> 00:01:06.840
All of them have to change.

00:01:07.300 --> 00:01:10.520
That's the exact inverse of the problem we had before.

00:01:11.380 --> 00:01:14.320
Procedural code makes it easy to add functions,

00:01:14.500 --> 00:01:18.040
while object oriented code makes it easy to add types.

00:01:18.700 --> 00:01:21.400
What's easy for one is hard for the other.

00:01:22.020 --> 00:01:24.240
So everything is not an object.

00:01:24.620 --> 00:01:26.860
Choose data structures with procedures

00:01:26.861 --> 00:01:29.081
when you expect to add new operations

00:01:29.660 --> 00:01:32.680
because none of your existing types need to change.

00:01:33.180 --> 00:01:36.320
Choose objects when you expect to add new types

00:01:36.580 --> 00:01:39.720
because none of your existing functions need to change.

00:01:40.340 --> 00:01:41.540
Know which kind of change

00:01:41.541 --> 00:01:43.841
Is coming and the design follows

00:01:44.620 --> 00:01:47.680
follow for more clean code principles coming next.

3. WEBVTT

00:00:00.000 --> 00:00:02.420
the law of Demeter has one rule

00:00:02.600 --> 00:00:05.060
talk to friends not to strangers

00:00:05.640 --> 00:00:09.180
a method should only call methods on the object it belongs to

00:00:09.520 --> 00:00:10.700
objects it creates

00:00:11.160 --> 00:00:14.860
objects past as arguments and objects it holds as fields

00:00:15.800 --> 00:00:18.980
never call methods on objects that those calls return

00:00:19.240 --> 00:00:21.460
this line does exactly that

00:00:21.560 --> 00:00:24.220
the function reaches through context to options

00:00:24.480 --> 00:00:26.660
through options to scratch directory

00:00:26.760 --> 00:00:31.260
through the directory to an absolute path three objects deep

00:00:31.320 --> 00:00:34.580
that's a lot of structural knowledge for one line of code

00:00:34.960 --> 00:00:37.140
but whether this violates Demeter

00:00:37.240 --> 00:00:40.300
depends on whether these are objects or data structures

00:00:40.840 --> 00:00:43.340
when it's just data there's no violation

00:00:43.880 --> 00:00:47.980
but add getters and the same access looks like a Demeter violation

00:00:48.520 --> 00:00:50.480
if their objects hiding behavior

00:00:50.481 --> 00:00:53.281
it is one if their data structures

00:00:53.282 --> 00:00:57.821
Demeter doesn't apply data is meant to expose its internals

00:00:58.280 --> 00:01:01.540
getters on data structures create false ambiguity

00:01:02.160 --> 00:01:03.920
so if these are real objects

00:01:03.921 --> 00:01:05.781
you shouldn't chain through them

00:01:06.040 --> 00:01:09.140
what if we just collapse the chain into one method

00:01:09.600 --> 00:01:12.620
the name encodes every object from that chain

00:01:12.960 --> 00:01:16.260
now every different combination needs its own method

00:01:16.720 --> 00:01:19.120
the structural knowledge didn't disappear

00:01:19.121 --> 00:01:25.081
it just moved the real solution is to ask why you need that path here

00:01:25.082 --> 00:01:29.461
to create a scratch file so tell the object what you need

00:01:29.760 --> 00:01:32.260
the chain collapses to a single call

00:01:32.320 --> 00:01:35.780
and your method knows nothing about the structure behind it

00:01:36.040 --> 00:01:37.580
that's the law of Demeter

00:01:38.080 --> 00:01:41.140
follow for more clean code principles coming next

4. WEBVTT

00:00:00.000 --> 00:00:02.300
some classes refuse to pick a side

00:00:02.480 --> 00:00:05.340
they expose their data through getters and setters

00:00:05.400 --> 00:00:08.460
but they also have methods that do real work

00:00:08.880 --> 00:00:13.200
this class does both it lets anyone read and write the price

00:00:13.201 --> 00:00:15.461
but it also calculates discounts

00:00:15.800 --> 00:00:18.460
so when a subscription comes along with different pricing

00:00:18.600 --> 00:00:21.820
the discount logic is trapped inside this class

00:00:22.240 --> 00:00:24.080
and when you need new behavior

00:00:24.081 --> 00:00:25.901
the data has already leaked

00:00:26.240 --> 00:00:29.140
external code uses the getters everywhere

00:00:29.400 --> 00:00:33.300
you've made it hard to add functions and hard to add types

00:00:33.560 --> 00:00:37.220
that's a hybrid the worst of both worlds

00:00:37.720 --> 00:00:40.860
but a pure data structure doesn't have this problem

00:00:41.080 --> 00:00:44.660
a DTO has public fields and no behaviour

00:00:44.720 --> 00:00:47.960
it carries data between your database and your code

00:00:47.961 --> 00:00:50.061
and that's all it needs to do

00:00:50.160 --> 00:00:52.340
active records look similar

00:00:52.600 --> 00:00:56.600
their data structures with navigational methods like save and delete

00:00:56.601 --> 00:00:59.101
that map directly to database rows

00:00:59.160 --> 00:01:00.900
and that's their job

00:01:01.200 --> 00:01:05.100
but the problem starts when developers add business logic

00:01:05.400 --> 00:01:07.760
now the class calculates discounts

00:01:07.761 --> 00:01:09.621
and you've got a hybrid again

00:01:09.680 --> 00:01:12.460
half data structure half object

00:01:12.760 --> 00:01:14.060
committed to neither

00:01:14.600 --> 00:01:17.380
the fix isn't removing save and delete

00:01:17.480 --> 00:01:20.320
it's treating the active record as what it is

00:01:20.321 --> 00:01:23.021
and putting the business rules somewhere else

00:01:23.160 --> 00:01:26.020
the pricing logic moves into its own object

00:01:26.120 --> 00:01:28.280
the active record stays clean

00:01:28.281 --> 00:01:31.221
and each class has one clear identity

00:01:31.720 --> 00:01:34.660
know what you're building and commit to it

00:01:35.160 --> 00:01:37.620
objects hide data and expose behaviour

00:01:38.160 --> 00:01:41.540
data structures expose data and skip the behaviour

00:01:42.000 --> 00:01:44.120
and the moment you try to do both

00:01:44.121 --> 00:01:46.701
you lose the advantages of each

00:01:47.200 --> 00:01:50.540
follow for more clean code principles coming next

## Error Handling

1. WEBVTT

00:00:00.040 --> 00:00:01.860
what does this function do

00:00:02.320 --> 00:00:05.120
take a moment somewhere inside the nesting

00:00:05.121 --> 00:00:07.761
there's an answer a sequence of steps

00:00:07.762 --> 00:00:09.261
that is the function

00:00:09.640 --> 00:00:12.600
but the error handling wraps every step so tightly

00:00:12.601 --> 00:00:14.341
that the algorithm disappears

00:00:14.520 --> 00:00:16.520
you're reading two things at once

00:00:16.521 --> 00:00:19.901
what happens when it works and what happens when it doesn't

00:00:19.960 --> 00:00:23.100
your eyes jump between the logic and the failure branches

00:00:23.360 --> 00:00:25.300
trying to hold both in your head

00:00:25.560 --> 00:00:27.900
and every new step makes it worse

00:00:28.080 --> 00:00:30.860
another check another level of nesting

00:00:31.040 --> 00:00:34.740
another LSP branch pushing the real work further from view

00:00:35.000 --> 00:00:37.340
that's the real cost of return codes

00:00:37.520 --> 00:00:40.140
they force two concerns into one structure

00:00:40.360 --> 00:00:42.580
and neither one is readable on its own

00:00:43.000 --> 00:00:45.400
now look at this same function

00:00:45.401 --> 00:00:46.541
with exceptions

00:00:47.080 --> 00:00:49.240
the error handling moves to one place

00:00:49.241 --> 00:00:51.581
and the algorithm stands on its own

00:00:51.840 --> 00:00:54.360
verify the session resolve the channel

00:00:54.361 --> 00:00:57.301
moderate the content broadcast to members

00:00:57.360 --> 00:01:00.980
four steps that's what the function does

00:01:01.160 --> 00:01:04.620
you couldn't see it before because every step was wrapped in a check

00:01:04.680 --> 00:01:07.620
and every check push the next step deeper

00:01:07.880 --> 00:01:11.100
with exceptions each concern is independent

00:01:11.440 --> 00:01:14.060
the algorithm doesn't know about error handling

00:01:14.080 --> 00:01:16.820
the error handling doesn't know about the algorithm

00:01:17.120 --> 00:01:20.380
you can read either one without the other getting in the way

00:01:20.640 --> 00:01:23.140
when two concerns share one function

00:01:23.560 --> 00:01:26.800
separate them let the algorithm be an algorithm

00:01:26.801 --> 00:01:28.701
and let the errors be errors

00:01:29.320 --> 00:01:32.780
follow for more clean code principles coming next

2. WEBVTT

00:00:00.020 --> 00:00:01.620
Write your try catch. Finally,

00:00:01.621 --> 00:00:04.841
first, when you expect the logic to throw an exception

00:00:04.940 --> 00:00:06.760
even before writing the logic,

00:00:06.980 --> 00:00:08.880
take this withdraw function.

00:00:08.940 --> 00:00:12.860
The whole code base runs fine as long as this function runs fine.

00:00:12.861 --> 00:00:17.081
But the moment it breaks, everything that depends on it breaks with it.

00:00:17.520 --> 00:00:20.560
Now, we could wrap the logic in error handling here,

00:00:20.580 --> 00:00:22.360
but let's try a different approach.

00:00:22.660 --> 00:00:24.680
Start with the try catch. Finally,

00:00:24.820 --> 00:00:28.000
we start by writing a test for the failure we expect.

00:00:28.060 --> 00:00:30.260
Let's say when something goes wrong here,

00:00:30.261 --> 00:00:32.921
this function should throw transaction failed.

00:00:33.100 --> 00:00:36.520
Our test fails since the function doesn't throw any error.

00:00:36.820 --> 00:00:37.940
So in the catch,

00:00:37.941 --> 00:00:41.601
we translate anything that gets thrown into transaction failed

00:00:42.060 --> 00:00:44.540
inside the try. We fetch an invalid account

00:00:44.541 --> 00:00:45.921
and the test passes.

00:00:46.220 --> 00:00:50.120
Every caller now knows this function can throw transaction failed.

00:00:50.220 --> 00:00:54.140
The try catch is the contract stating what the function handles

00:00:54.141 --> 00:00:56.001
and what the caller should expect.

00:00:56.180 --> 00:00:59.560
And the tests that were breaking across the code base go green

00:00:59.620 --> 00:01:02.820
because every caller knows what to expect from this function

00:01:02.821 --> 00:01:05.181
and handles it. And from here,

00:01:05.182 --> 00:01:08.721
anything we add inside the try stays inside the contract.

00:01:08.900 --> 00:01:13.140
So write it first. Define the contract before the logic,

00:01:13.141 --> 00:01:15.641
and whatever you add after stays contained.

00:01:15.740 --> 00:01:18.440
No other part of the system breaks with it.

00:01:18.780 --> 00:01:21.960
Follow for more clean code principles coming next.

3. WEBVTT

00:00:00.060 --> 00:00:03.200
Exception types are part of your code's design,

00:00:03.260 --> 00:00:06.500
but if you're catching a library's exceptions directly,

00:00:06.501 --> 00:00:09.321
you've inherited the library's shape as your own.

00:00:09.700 --> 00:00:13.780
Look at this. Catch block 3 exception types from the library,

00:00:13.781 --> 00:00:17.041
but the code handles all three the same way.

00:00:17.300 --> 00:00:20.040
These aren't distinctions your code needs.

00:00:20.060 --> 00:00:22.400
They're distinctions the library has.

00:00:22.780 --> 00:00:26.300
Direct dependency on. A library's structure is the problem.

00:00:26.301 --> 00:00:29.421
Your code base shouldn't be tightly coupled to it.

00:00:29.422 --> 00:00:32.241
Your code should have a structure you chose,

00:00:32.460 --> 00:00:34.660
but you can't change the library.

00:00:34.661 --> 00:00:38.401
So how do you get there? Put a class in between.

00:00:38.660 --> 00:00:40.720
The wrapper holds the library.

00:00:40.780 --> 00:00:43.060
It knows the library's exception types

00:00:43.061 --> 00:00:46.841
and translates them into whatever your system actually needs.

00:00:47.020 --> 00:00:48.840
Maybe that's one exception,

00:00:48.860 --> 00:00:51.200
maybe it's a different split entirely.

00:00:51.420 --> 00:00:56.000
Either way, the types your code catches are types you defined.

00:00:56.300 --> 00:00:58.600
From there, everything gets cleaner.

00:00:58.780 --> 00:01:02.160
The wrapper is the library's connector to your code.

00:01:02.180 --> 00:01:04.720
It also makes the library swappable.

00:01:04.860 --> 00:01:08.740
Want to replace S3 with Google Cloud Storage only?

00:01:08.741 --> 00:01:10.641
The wrapper needs to be updated.

00:01:10.660 --> 00:01:13.980
Everything else in your system uses the same API

00:01:13.981 --> 00:01:18.481
your wrapper defined and catches the same storage failure exception.

00:01:18.940 --> 00:01:22.120
Exception types are part of your code's design.

00:01:22.140 --> 00:01:23.620
They should belong to you,

00:01:23.621 --> 00:01:26.601
not to whichever library you happens to install.

00:01:26.900 --> 00:01:31.360
Wrap third party APIs and design becomes a decision again.

00:01:31.660 --> 00:01:35.120
Follow for more clean code principles coming next.

4. This code calculates tax for an order. It looks up the rule for the order's region, applies it to the subtotal, and adds the result to the total. When no rule matches the region, the lookup throws an exception, and the catch block handles it by using the standard rate instead. But if we look at the actual flow, the catch is acting as a condition rather than an edge case. The calculation can go two ways, both normal, both producing tax. The exception isn't catching something that broke. It's catching one of the two regular paths the logic expects to take. So this shouldn't be an exception, and there's a better way to handle that. If we review this function, it returns a rule for known regions and throws when none matches. We make a tax rule for the default tax, same shape as the regional rules. Then in the lookup, we return that instead of throwing an exception. Now the lookup never fails, and the caller doesn't need exception handling anymore. The existing flow that we had, it now becomes simpler. It's just one path with no exception. Exceptions are for what actually breaks, not for branches the code already plans for. Follow for more clean code principles coming next.

5. When a method returns null, every caller has to guard against it. This is why this code looks like a pyramid, where each level checks the result of the call below. A missed check anywhere becomes a null pointer exception at runtime, usually caught far from where the problem started. This is the kind of code we want to avoid, and the fix isn't writing more checks. It's having fewer methods return null in the first place. We can't eliminate every one, but we can fix most. Take getOrders. When there are no orders, returning an empty list works just as well, since iterating an empty list does nothing, which is exactly what no orders should mean. The outer check is no longer needed. Same idea for the discount. Returning zero when there isn't one means subtracting zero does nothing, so the result stays the same. The inner check disappears too, and the pyramid flattens to a single loop. This works when the absence has a sensible value, where no orders is an empty list and no discount is zero. But null isn't always wrong. Sometimes null is the answer. The signed-in user might be null, and the caller checks that as part of the logic, not as a defense. What's left are the edge cases where something has actually gone wrong and returning null fails silently. Throw an exception instead. An exception names the cause and points to where it broke so you can trace it and handle it at the right level. Follow for more clean code principles coming next.

## Boundaries

1. There's nothing wrong with this checkout function.
   It imports the payment SDK and calls it right where the charge happens,
   exactly like the dogs show.
   So the rest of your code base did the same thing everywhere.
   One search and you can see how deep it reaches into your code
   and it all works until there's a breaking change from the SDK.
   The new major version removes the old charge call
   and the build breaks everywhere it was used.
   You can't stop a library from changing,
   but what you control is how much of your code calls it directly.
   Fixing every broken file would work,
   but only until the next change.
   So instead, you wrap the SDK in one small class
   that does what your app actually needs.
   Charge an order, refund a payment.
   And the SDK's details stay hidden inside it.
   So checkout calls your class instead.
   In words, your app owns.
   When the SDK has a breaking change, again,
   only the wrapper needs to be updated
   and nothing else in your code base needs to change.
   Every 3rd party library sits at a boundary,
   wrap it, and you depend on code you own,
   not code you don't follow.
   For more clean code principles, coming next.

2. Sometimes the piece your code needs isn't ready yet,
   maybe because the team responsible hasn't built it
   or they haven't finalized the library.
   Instead of stopping your work,
   you can write the interface you wish you had.
   Its shape comes directly from what your own code needs.
   In this case, you provide the amount and card details,
   then expect a receipt back.
   Checkout takes it as an argument,
   and now you can write the real call.
   Even though nothing behind it exists yet.
   It only has to implement that interface.
   So a fake that approves every charge is enough for now.
   The tests pass and they're testing your logic,
   not theirs. Once the provider is picked,
   you can finally build against the real thing,
   but it may look nothing like the interface you wrote here.
   It wants cents instead of dollars and a token instead of the card.
   That mismatch has to be resolved somewhere,
   and the one place it must not spread
   is into the code you've already finished.
   So it all goes into one new class instead,
   an adapter that implements your interface and calls theirs.
   An adapter is really just a translator
   taking what your code says
   and repeating it the way the provider needs to hear it.
   Now, if you look back at checkout,
   not a single line of it has changed.
   Write the interface you need,
   build against it today,
   and let one adapter connect it to whatever finally ships.
   Follow for more clean code Principles coming next.

## Function Design

Every function you write belongs to a context.
That context is a cooperative grouping of functions
and the data they share.
Inside that grouping,
the public interface sits at a higher level to describe what it does,
while the private internal sit below to handle how.
That boundary is really a decision about change.
It marks what you expect to hold still
and what you expect to keep moving.
To see what happens when that split goes wrong,
take a context designed to send order emails.
Because its general send helper was left public,
other modules reach straight for it
whenever the interface lacks what they need.
So when the delivery format changes,
every external call that depended on how emails are sent has to change
too. By moving that helper private,
you force those external use cases inside as dedicated public events.
Now, the next time the delivery mechanism changes,
the entire update is contained right here.
In the end, the boundary you draw is your intent.
Expose the high level concepts that hold still
and hide the low level details that change.
Follow for more clean code principles coming next.

By every standard test for good naming,
this function looks completely fine.
It is clear, searchable,
and tells you exactly what the comparison inside does.
The flaw is that it restates the implementation
when it should be explaining what that implementation is for.
When the name sits one level above the implementation,
it describes what the code achieves and hides how it is done.
Every place that calls it now reads as clear intent
while the implementation remains free to evolve.
The rule applies to every function you write.
Keep the name one level of abstraction above the code,
describing the concept rather than the implementation.
Follow for more clean code principles coming next.

The wider a variable's scope,
the longer its name needs to be.
But for functions, that rule runs completely backwards.
For variables, that makes intuitive sense.
When something only lives for a line or two,
even a single letter is fine
because nothing else in scope is competing with it.
But widen that scope to multiple files
and you need descriptive words
so it does not collide with everything around it.
With functions, though,
that dynamic flips,
a narrow scope is what actually forces names to be longer
and more specific. You can see why in this importer class,
where eight private helpers all handle different file operations.
Because they all live in the same narrow context,
doing subtle variations of the same job,
extra words are essential just to tell them apart.
Push that scope out to the whole code base, though,
and functions represent distinct general operations
where a single verb says everything.
And because they get called from everywhere,
keeping that name short makes every call site clean and convenient.
So before you debate how long a function's name should be,
look at how wide its scope actually is.
Follow for more clean code principles coming next.

## Classes

Words like manager and processor in a class name
are almost always a warning sign.
They are casual words you reach for when a class lacks a single
clear responsibility.
Take this order manager. Half of it prices an order
and the other half talks to the payment gateway.
You might try to clean it up by giving it a more specific name
like order pricing, but that name is a lie
because a class named for arithmetic
is still charging cards and issuing refunds.
To make the name honest, you have to name both jobs.
And that brings us to the real issue.
Whenever you need an and, the class is doing multiple things.
So stop trying to rename it
and split the class right where the and sits.
With the responsibilities separated,
both classes get obvious. Honest names.
A class name is a measurement of the code behind it,
not a label you choose.
If you can't name a class with a single noun phrase,
split it until you can follow.
For more clean code principles, coming next.

At first glance, there is nothing wrong with this method.
It takes three arguments,
runs a pure calculation and returns the result.
But look closer
and you notice every argument is coming from the same invoice.
That cost becomes obvious the moment invoices gain a new field
like a credit. In response,
it might seem like the problem is the growing argument list
and the fix is to simply pass the entire invoice.
But if all the data belongs to the invoice,
why is this method on billing service?
Because
when a function takes most of its arguments from another object,
it is trying hard to be part of that object.
So move the method onto invoice
and all those arguments disappear on their own.
Now the caller simply asks for what is due
without needing to know a single internal detail.
When a function needs a lot of arguments,
the fix might not be a shorter list,
but a different home follow.
For more clean code principles coming next.

When a function gets too big,
it starts looking like a class.
Take this long function. At the top,
you have local variables,
and underneath are blocks of code behaving like methods.
A proper class gives you clear names and boundaries,
but here everything is tangled in one place,
making it hard to understand the logic.
See clear boundaries or safely refactor it.
Our goal is to separate these responsibilities into distinct classes
with clear boundaries. But here,
even simple extraction breaks down
because almost every block reads and mutates the same local variables,
forcing you to pass state back and forth.
You can bypass that by promoting those locals into fields,
letting you extract every block without passing any arguments.
But this is only the first step.
Next, we track which fields each method touches
to see which logic actually belongs together.
Methods that share the same data form natural groups,
which you can now pull out into their own dedicated classes.
With all that work moved out,
the original function now only coordinates them.
Shorter functions make code easier to read,
but keeping logic with its data is what makes it easy to change.
Follow for more clean code. Principles coming next.

A module can declare the steps of a workflow
and delegate every one of them,
or it can implement the specific details of one of those steps.
What it should never do is both
mixing policy with implementation detail.
Take this checkout service where four steps delegate cleanly,
but a block of pricing math sits right in the middle.
A clean module should have only one reason to change here
when policy changes
to reserve stock first and deduct only after payment,
the workflow steps need to change.
And when shipping rates increase,
you have to edit the same module.
That is a violation of the single responsibility principle.
To fix it, move the implementation details out into a separate class
so the workflow only has to delegate.
Now a policy change only touches the workflow,
and a detail change only touches the class that does the work.
So for every file you write,
ask whether your module is declaring or doing,
and if the answer is both,
move the detail out. Follow for more clean code principles coming next.

Most refactoring starts the same way.
You spot messy code and you clean it up.
But when you refactor on a guess,
you can end up adding awkward conditions
just to make the next requirement fit.
Take this discount system.
Each coupon applies a different percentage of the price.
These cases all do the same calculation,
only the percentage changes.
To simplify, we can put the percentages in a map
and replace the switch with one formula.
Now adding another percentage coupon takes just one new entry.
But what if the next coupon takes a fixed amount off the price?
Now the function needs a condition to choose which calculation to use.
When we design around a guess,
each new requirement can push the code
further from the simplicity we wanted.
So instead of guessing what comes next,
let's go back and wait for a real requirement.
If the change fits the logic we already have,
we can simply add it. But if the change needs different logic,
first reshape the code without changing its behaviour
so the new logic can be added separately.
Here we move the percentage calculation into its own class.
We give each coupon its percentage,
then let the function delegate the calculation.
Now we can add the new behaviour in its own class
without changing the calculation that already works.
The real change showed us where we needed flexibility.
Now the refactor supports other variations too.
So if the code already works,
we can leave It alone
until a real requirement gives us a reason to refactor.
Then we make room for that change
without altering the existing behavior.
And then add the new feature.
Follow for more clean code principles coming next.

Almost every rule about clean code points in the same direction.
Keep classes small,
give each one a single job so it has one reason to change.
Name it in one clear phrase
and keep the decisions apart from the details.
Every one of them turns one class into many.
And generally that is what we want
because it allows a feature to land as a new class
without much changes to existing code.
But nothing in those rules says stop.
You can keep splitting and past a certain point the pieces add nothing.
That is over engineering. So how far do you take it?
Only as far as the next class still does something for you.
And there are only four things it can do.
It can let you test one piece on its own
so you can check it without running everything around it.
It can remove code that was written twice
so a fix only has to be made once.
It can give a name to something that never had one
so the next person can find it.
Or it can hold new behaviour
so nothing that already works has to change.
Anything past that is an element you did not need.
And the last rule of simple design
is to have as few of those as you can
follow. For more clean code principles coming next.

## Solid

Single responsibility principle says every class should have one job
and only one. A job is the one thing the class is in charge of,
and every method in it should serve it.
The moment you add methods that serve a different purpose,
the class takes on a second job.
You can usually see it right in the method list,
where the methods fall into distinct groups,
each doing its own kind of work.
Because the principle allows only one job per class,
we have to split those groups into classes of their own.
Now, any new requirement belongs to a single job,
so it lands in just one class.
Take this invoice class. It calculates what the customer owes,
builds the email, and sends it.
A change to tax rules forces an update to pricing,
and an overdue reminder forces a change to email delivery,
all in the exact same class.
It is changing for two very different reasons,
and that breaks the principle.
When each job gets its own class,
a change to one can no longer break the other.
Whenever you write a class,
ask what would make you change it.
More than one answer means more than one class.
But what exactly counts as a reason to change?
That's where most people get this principle wrong,
and it's what we cover in the next lesson.
Follow for more engineering principles coming next.
