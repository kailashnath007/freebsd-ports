# Created by: David O'Brien (obrien@NUXI.com)
# $FreeBSD$

PORTNAME=	gag
PORTVERSION=	2.9
CATEGORIES=	security
MASTER_SITES=	http://staff.washington.edu/dittrich/misc/
DISTNAME=	sickenscan
EXTRACT_SUFX=	.tar

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Stacheldraht (DOS attack) agent detector

LATEST_LINK=	gag-sickenscan

ALL_TARGET=	gag

PORTDOCS=	README
PLIST_FILES=	sbin/gag

OPTIONS_DEFINE=	DOCS

do-install:
	@${INSTALL_PROGRAM} ${WRKSRC}/gag ${STAGEDIR}${PREFIX}/sbin
	${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_MAN} ${WRKSRC}/${PORTDOCS} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
