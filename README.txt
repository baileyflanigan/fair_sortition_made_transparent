code files provided:
	paper_data_analysis.py: runs all analysis
	paper_data_visualization.py: produces all plots

input data format (as specified on Panelot.org):
	For each instance, should have the following data:
		categories.csv - contains all quotas on all features and their values
		respondents.csv - contains all features and values of all respondents
	
	Instructions: put each instance's files in a separate folder, each titled <instance shortname>_k (k = number of participants being put on the panel)




To reproduce Figure 1:

Step 1. run paper_data_analysis.py with the following parameter settings:

	# # # # # # # # # # # # # # PARAMETERS # # # # # # # # # # # # # # # # #

	# number of panels desired in the lottery
	M = 1000

	# which instances to analyze
	instances = ['sf_a_35', 'sf_b_20', 'sf_c_44', 'sf_d_40', 'sf_e_110', 'cca_75', 'hd_30', 'mass_24','nexus_170','obf_30','newd_40']


	# which objective you want to optimize
	LEXIMIN = 0
	MAXIMIN = 1
	NASH = 0

	# flags for which types of lotteries you want to compute
	OPT = 1                      # computes unconstrained optimal distribution - need to run before any others

	ILP = 1                      # computes both optimal unconstrained and near-optimal unconstrained, wrt to fairness notion specified below
	BECK_FIALA = 1               # computes uniform rounded from OPT via beck-fiala (must run OPT first)
	RANDOMIZED = 1               # computes uniform rounded from OPT via randomized rounding (must run OPT first) 
	RANDOMIZED_REPLICATES = 1000 # runs randomized a bunch of times -> report avg and stdev of loss
	ILP_MINIMIAX_CHANGE = 0      # takes input distribution specified by fairness objectives and computes minimum change in anyone's probability

	# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #

Step 2. run paper_data_visualization.py with the following parameter settings:

	# # # # # # # # # # # # # # PARAMETERS # # # # # # # # # # # # # # # # #

	# number of panels desired in the lottery
	M = 1000

	# instances you want to run plots for
	instances = ['sf_a_35', 'sf_b_20', 'sf_c_44', 'sf_d_40', 'sf_e_110', 'cca_75', 'hd_30', 'mass_24','nexus_170','obf_30','newd_40']
	instance_names_dict = {'sf_a_35':'sf(a)', 'sf_b_20': 'sf(b)', 'sf_c_44':'sf(c)', 'sf_d_40':'sf(d)', 'sf_e_110':'sf(e)', 'cca_75':'cca', 'hd_30':'hd', 'mass_24':'mass','nexus_170':'nexus','obf_30':'obf','newd_40':'ndem'}

	# objectives (can only run one at a time)
	LEXIMIN = 0
	MAXIMIN = 1
	NASH = 0

	# which rounding algorithms to analyze
	ILP = 1  
	ILP_MINIMAX_CHANGE = 0                
	BECK_FIALA = 1
	RANDOMIZED = 1
	RANDOMIZED_REPLICATES = 1000
	THEORY = 1

	# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #






To reproduce Nash Welfare analog of Figure 1 (in Appendix E.3):

Step 1. run paper_data_analysis.py with the following parameter settings:

	# # # # # # # # # # # # # # PARAMETERS # # # # # # # # # # # # # # # # #

	# number of panels desired in the lottery
	M = 1000

	# which instances to analyze
	instances = ['sf_a_35', 'sf_b_20', 'sf_c_44', 'sf_d_40', 'sf_e_110', 'cca_75', 'hd_30', 'mass_24','nexus_170','obf_30','newd_40']


	# which objective you want to optimize
	LEXIMIN = 0
	MAXIMIN = 0
	NASH = 1

	# flags for which types of lotteries you want to compute
	OPT = 1                      # computes unconstrained optimal distribution - need to run before any others

	ILP = 1                      # computes both optimal unconstrained and near-optimal unconstrained, wrt to fairness notion specified below
	BECK_FIALA = 1               # computes uniform rounded from OPT via beck-fiala (must run OPT first)
	RANDOMIZED = 1               # computes uniform rounded from OPT via randomized rounding (must run OPT first) 
	RANDOMIZED_REPLICATES = 1000 # runs randomized a bunch of times -> report avg and stdev of loss
	ILP_MINIMIAX_CHANGE = 0      # takes input distribution specified by fairness objectives and computes minimum change in anyone's probability

	# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #

Step 2. run paper_data_visualization.py with the following parameter settings:

	# # # # # # # # # # # # # # PARAMETERS # # # # # # # # # # # # # # # # #

	# number of panels desired in the lottery
	M = 1000

	# instances you want to run plots for
	instances = ['sf_a_35', 'sf_b_20', 'sf_c_44', 'sf_d_40', 'sf_e_110', 'cca_75', 'hd_30', 'mass_24','nexus_170','obf_30','newd_40']
	instance_names_dict = {'sf_a_35':'sf(a)', 'sf_b_20': 'sf(b)', 'sf_c_44':'sf(c)', 'sf_d_40':'sf(d)', 'sf_e_110':'sf(e)', 'cca_75':'cca', 'hd_30':'hd', 'mass_24':'mass','nexus_170':'nexus','obf_30':'obf','newd_40':'ndem'}

	# objectives (can only run one at a time)
	LEXIMIN = 0
	MAXIMIN = 0
	NASH = 1

	# which rounding algorithms to analyze
	ILP = 1  
	ILP_MINIMAX_CHANGE = 0                
	BECK_FIALA = 1
	RANDOMIZED = 1
	RANDOMIZED_REPLICATES = 1000
	THEORY = 1

	# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #







To reproduce Figure 2 plus all analogous figures in Appendix E.4:

Step 1. run paper_data_analysis.py with the following parameter settings:

	# # # # # # # # # # # # # # PARAMETERS # # # # # # # # # # # # # # # # #

	# number of panels desired in the lottery
	M = 1000

	# which instances to analyze
	instances = ['sf_a_35', 'sf_b_20', 'sf_c_44', 'sf_d_40', 'sf_e_110', 'cca_75', 'hd_30', 'mass_24','nexus_170','obf_30','newd_40']


	# which objective you want to optimize
	LEXIMIN = 1
	MAXIMIN = 0
	NASH = 0

	# flags for which types of lotteries you want to compute
	OPT = 1                      # computes unconstrained optimal distribution - need to run before any others

	ILP = 0                      # computes both optimal unconstrained and near-optimal unconstrained, wrt to fairness notion specified below
	BECK_FIALA = 1               # computes uniform rounded from OPT via beck-fiala (must run OPT first)
	RANDOMIZED = 1               # computes uniform rounded from OPT via randomized rounding (must run OPT first) 
	RANDOMIZED_REPLICATES = 1000 # runs randomized a bunch of times -> report avg and stdev of loss
	ILP_MINIMIAX_CHANGE = 1      # takes input distribution specified by fairness objectives and computes minimum change in anyone's probability

	# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #

Step 2. run paper_data_visualization.py with the following parameter settings

	# # # # # # # # # # # # # # PARAMETERS # # # # # # # # # # # # # # # # #

	# number of panels desired in the lottery
	M = 1000

	# instances you want to run plots for
	instances = ['sf_a_35', 'sf_b_20', 'sf_c_44', 'sf_d_40', 'sf_e_110', 'cca_75', 'hd_30', 'mass_24','nexus_170','obf_30','newd_40']
	instance_names_dict = {'sf_a_35':'sf(a)', 'sf_b_20': 'sf(b)', 'sf_c_44':'sf(c)', 'sf_d_40':'sf(d)', 'sf_e_110':'sf(e)', 'cca_75':'cca', 'hd_30':'hd', 'mass_24':'mass','nexus_170':'nexus','obf_30':'obf','newd_40':'ndem'}

	# objectives (can only run one at a time)
	LEXIMIN = 1
	MAXIMIN = 0
	NASH = 0

	# which rounding algorithms to analyze
	ILP = 0  
	ILP_MINIMAX_CHANGE = 1                
	BECK_FIALA = 1
	RANDOMIZED = 1
	RANDOMIZED_REPLICATES = 1000
	THEORY = 1

	# # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #



