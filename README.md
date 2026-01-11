# Flight Pricing Analytics Dashboard

## Project Overview

This Power BI dashboard provides comprehensive analytics for flight booking data, enabling data-driven decision-making for revenue optimization, route planning, and competitive positioning. The dashboard transforms raw flight booking data into actionable insights through interactive visualizations and strategic metrics across four specialized pages.

## Business Objective

The primary goal of this project is to empower revenue management teams and airline executives to optimize pricing strategies, identify profitable routes, and maintain competitive market positioning. By analyzing key variables including pricing trends, booking patterns, route performance, and competitive benchmarks, stakeholders can make informed decisions that maximize revenue while meeting customer demand.

## Target Users

**Primary Users:**
- Revenue Management Analysts: Daily pricing optimization and demand forecasting
- Airline Executives: Strategic planning and performance oversight
- Route Planning Teams: Network optimization and capacity allocation
- Marketing Teams: Promotional campaign planning and customer insights
- Data Scientists & Analysts: Deep-dive exploration and model development

## Key Business Questions Addressed

This dashboard answers critical business questions including:
- How should tickets be priced based on booking window and route characteristics?
- Which routes generate the highest revenue and demand?
- How do our airlines compare competitively on pricing and service offerings?
- What is the optimal pricing strategy for Business vs Economy class?
- When do customers typically book, and how does timing affect pricing power?
- What is the impact of stops and flight duration on customer willingness to pay?
- Which routes should be expanded, optimized, or discontinued?
- What are the granular patterns in specific flight segments for detailed investigation?

## Dashboard Structure

### Page 1: Executive Overview

A high-level snapshot providing instant visibility into overall performance and key trends. This landing page features critical KPIs including total flights, average pricing, flight duration, and route coverage. Interactive visualizations reveal pricing trends by booking window, top-performing routes, airline competitive positioning, and class distribution. Comprehensive slicers enable users to filter data by airline, cities, class, and stops for customized analysis.

**Components:**
- Top Section (KPI Cards): Total Flights, Average Price, Average Duration, Total Routes
- Price Trends: Line chart showing Price vs Days Left with slicer for Class
- Route Performance: Bar chart displaying Top 10 routes by average price
- Airline Comparison: Grouped bar chart comparing Airlines by Average Price, Flight Count, Average Duration
- Class Distribution: Donut chart showing Business vs Economy split
- Key Slicers (Sidebar): Airline, Source City, Destination City, Class, Stops

**Key Insights Delivered:**
- Overall flight network performance at a glance
- Pricing trend analysis by booking window
- Top revenue-generating routes
- Competitive airline benchmarking across multiple metrics
- Business vs Economy class distribution patterns

### Page 2: Route & Pricing Deep Dive

An analytical deep-dive focused on pricing optimization and route performance. This page leverages advanced visualizations including city-pair heatmaps, duration-price correlation scatter plots, and booking window analysis segmented by stops. The time-based pricing analysis reveals how departure times influence pricing power, while detailed route tables with conditional formatting highlight performance outliers and opportunities.

**Components:**
- Heatmap: Source City × Destination City (color-coded by average price)
- Scatter Plot: Duration vs Price (size = flight count, color = stops)
- Price by Booking Window: Line chart showing Price by Days Left segmented by Stops
- Time Analysis: Clustered bar chart showing Average Price by Departure Time and Class
- Route Details Table: Source, Destination, Flights, Average Price, Average Duration (with conditional formatting)
- Slicers: Days Left range, Departure Time, Arrival Time

**Key Insights Delivered:**
- Route-level pricing patterns and premium opportunities
- Optimal booking windows for different customer segments
- Impact of flight duration and stops on pricing
- Time-of-day pricing dynamics by class
- Granular route performance metrics for strategic planning

### Page 3: Airline & Class Performance

A competitive intelligence page providing comparative analysis across airlines and service classes. Matrix visualizations with conditional formatting enable quick performance assessment, while class premium analysis reveals pricing strategies and market positioning. Market share breakdowns and stop analysis provide insights into competitive advantages and product differentiation opportunities.

**Components:**
- Airline Matrix: Heatmap/table with conditional formatting (Airline × Metrics)
- Class Premium Analysis: Stacked bar chart showing price difference between Business and Economy by airline
- Market Share: Stacked column chart displaying flight count by airline and class
- Stop Analysis: Clustered column chart showing Average Price by Stops and Class
- Airline Routes: Table showing routes served per airline with average pricing
- Slicers: Airline, Class, Source/Destination cities

**Key Insights Delivered:**
- Comprehensive airline performance comparison across key metrics
- Business class pricing premium analysis by airline
- Market share distribution by airline and service class
- Stop penalty quantification and its impact on pricing
- Route coverage and pricing strategy by airline

### Page 4: Detailed Data Explorer

A comprehensive data exploration page designed for power users, analysts, and data scientists who require granular access to the underlying dataset. This page features a detailed data table displaying all flight records with complete attribute information, advanced multi-dimensional filtering capabilities, and search functionality for specific flight codes or routes. Users can apply complex filter combinations, export filtered datasets for external analysis, and conduct ad-hoc investigations beyond pre-built visualizations.

**Components:**
- Complete data table with all 11 variables (sortable and filterable)
- Advanced slicer panel for multi-attribute filtering
- Search functionality for specific flights, routes, or airlines
- Data export capability for offline analysis or reporting
- Row-level detail access for anomaly investigation and validation
- Dynamic filtering synchronized with other dashboard pages
- Column-level conditional formatting for quick pattern recognition

**Use Cases:**
- Investigating specific pricing anomalies or outliers
- Extracting custom datasets for machine learning model development
- Validating aggregated metrics from other dashboard pages
- Conducting ad-hoc analysis for unique business questions
- Supporting audit and compliance requirements
- Exporting data subsets for stakeholder presentations

## Dataset Features

The dashboard analyzes 11 key variables from the flight booking dataset:

**Categorical Variables:**
- Airline: 6 different airline companies
- Flight: Flight code identifier
- Source City: 6 unique departure cities
- Destination City: 6 unique arrival cities
- Departure Time: 6 time period bins
- Arrival Time: 6 time period bins
- Stops: 3 levels (direct, 1 stop, 2+ stops)
- Class: 2 categories (Business, Economy)

**Continuous Variables:**
- Duration: Total flight time in hours
- Days Left: Booking window (days between booking and departure)
- Price: Ticket price (target variable)

## Design Principles

The dashboard follows modern data visualization best practices:

- **Clarity First:** Clean layouts with purposeful white space and intuitive navigation
- **Interactivity:** Cross-filtering between visuals and synchronized slicers for exploratory analysis
- **Progressive Disclosure:** From high-level overview to granular data access, matching user expertise levels
- **Performance-Optimized:** Efficient DAX measures and optimized data model for responsive user experience
- **Actionable Insights:** Every visualization answers specific business questions with clear takeaways
- **Self-Service Analytics:** Empowering users to explore data independently through the Detailed Data Explorer

## Technical Implementation

**Tools & Technologies:**
- Power BI Desktop for dashboard development
- Power Query for data transformation and cleaning
- DAX (Data Analysis Expressions) for calculated measures and KPIs
- Conditional formatting and visual-level filters for enhanced interactivity
- Table visual with advanced filtering for data exploration

**Key DAX Measures:**
- Average Price by multiple dimensions (route, airline, class, booking window)
- Total Routes (distinct source-destination pairs)
- Price variance and premium calculations
- Flight count and route coverage metrics
- Performance rankings and comparative indices
- Dynamic row count for filtered data display

**Data Model:**
- Single fact table architecture for optimal performance
- Calculated columns for derived attributes (Route, Time bins)
- Measure tables for organized DAX calculations
- Proper data type assignments for all fields
- Relationships configured for cross-filtering functionality

## Expected Outcomes

By implementing this dashboard, organizations can expect:

- **Revenue Optimization:** Data-driven pricing strategies based on demand patterns and competitive positioning
- **Strategic Route Planning:** Identify expansion opportunities and underperforming routes
- **Competitive Intelligence:** Real-time benchmarking against competitor airlines
- **Operational Efficiency:** Optimize flight schedules based on demand and pricing power
- **Improved Decision Speed:** Reduce analysis time from hours to minutes with interactive self-service analytics
- **Enhanced Data Accessibility:** Empower all user levels from executives to data scientists with appropriate detail
- **Audit & Validation:** Enable data verification and quality assurance through granular record access

## Future Enhancements

Potential extensions to this project include:

- Predictive pricing models using machine learning
- Real-time data integration for dynamic pricing
- Customer segmentation analysis
- Seasonal and temporal pattern analysis with date intelligence
- Mobile-optimized dashboard version
- Automated alerts for pricing anomalies or competitive threats
- Integration with booking systems for live pricing updates
- Advanced analytics with Python/R integration in Power BI
- Geospatial visualizations with route mapping
- Customer sentiment analysis integration

## Project Summary

This Flight Pricing Analytics Dashboard transforms complex flight booking data into clear, actionable insights through a comprehensive four-page Power BI solution. Designed to serve multiple user personas—from executives requiring high-level summaries to data scientists needing granular data access—it combines strategic overview, detailed pricing analytics, competitive intelligence, and flexible data exploration. This multi-layered approach supports strategic decision-making and revenue optimization across all organizational levels in the highly competitive airline industry.

## User Journey

**Executive User:**  
Page 1 (Quick insights) → Exit or drill to Pages 2-3 for specific questions

**Revenue Analyst:**  
Page 1 (Overview) → Page 2 (Pricing analysis) → Page 4 (Validate specific data points)

**Data Scientist:**  
Page 4 (Explore patterns) → Pages 1-3 (Validate hypotheses) → Page 4 (Export for modeling)

**Route Planner:**  
Page 1 (Performance check) → Page 2 (Route details) → Page 3 (Competitive context)

## Getting Started

**Prerequisites:**
- Power BI Desktop (latest version recommended)
- Flight booking dataset (CSV/Excel format)
- Basic understanding of Power BI navigation

**Installation Steps:**
1. Clone or download the project repository
2. Open the .pbix file in Power BI Desktop
3. Update data source connection if necessary
4. Refresh data to load the latest dataset
5. Navigate through pages using page tabs or navigation buttons

## Contributors

This project was developed as part of a data analytics initiative to demonstrate Power BI capabilities in the airline industry domain.

## License

This project is intended for educational and portfolio purposes.

---

**Last Updated:** January 2026  
**Version:** 1.0  
**Contact:** For questions or feedback, please refer to the project repository.
